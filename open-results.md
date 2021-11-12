---
layout: content-without-sidebar
title: Open Contest Results
key: open-results
---

<link rel="stylesheet" href="assets/css/scoreboard.css">

<style>
@media (min-width: 768px) {
  .open-container {
    width: 750px !important;
  }
}

@media (min-width: 992px) {
  .open-container {
    width: 970px !important;
  }
}


@media (min-width: 1200px) {
  .open-container {
    width: 1170px !important;
  }
}
</style>

<div class="container open-container">
<div class="row">
<div class="col-md-12">

<p>Medals are awarded based on the cutoffs from the actual competition.</p>
<p><i><u>For Indonesian citizens only</u>: Para pemenang hadiah kategori umum dan siswa akan dihubungi via email.</i></p>

<form>
  <label for="filter">Filter By Team: </label>
  <select id="filter" style="width:auto">
  </select>
</form>
<table id="results" class="table table-bordered table-hover table-condensed"></table>

</div>
</div>
</div>

<script>
  const country_index = 1;
  const medal_index = 3;
  var data = [];
  var table_el = document.getElementById("results");
  var filter_el = document.getElementById("filter");
  var countries = [ "All Teams" ];
  
  function onlyUniqueNoEmpty(value, index, self) { 
    return self.indexOf(value) === index && value !== "";
  }

  function populateCountries() {
    countries = countries.concat(data.map(c => c[country_index])
                .slice(1).filter(onlyUniqueNoEmpty).sort());
  }
  
  function h (parent, tag) {
    var el = document.createElement(tag);
    parent.append(el);
    return el;
  }

  function httpGetAsync(theUrl, callback)
  {
    var xmlHttp = new XMLHttpRequest();
    xmlHttp.onreadystatechange = function() { 
      if (xmlHttp.readyState == 4 && xmlHttp.status == 200)
        callback(xmlHttp.responseText);
    }
    xmlHttp.open("GET", theUrl, true); // true for asynchronous 
    xmlHttp.send(null);
  }

  function processCSV(allText) {
    var allTextLines = allText.split(/\r\n|\n/);
    var lines = [];

    for (var i=0; i<allTextLines.length; i++) {
      var data = allTextLines[i].split('\t');
      lines.push(data);
    }

    return lines;
  }

  function onFilterChange(e) {
    populateTable(
      table_el, 
      [data[0]].concat(data.slice(1).filter(c => 
        e.target.value === "All Teams"
        || e.target.value === c[country_index]))
    );
  }

  function populateFilter() {
    filter_el.addEventListener("change", onFilterChange);
    for (var i = 0; i<countries.length; i++) {
      var option = h(filter_el, "option");
      option.textContent = countries[i];
      option.value = countries[i];
    }
  }

  function populateTable(table, data) {
    table.innerHTML = "";
    var thead = h(table, "thead");
    var thead_tr = h(thead, "tr");
    for (var j=0; j<data[0].length; j++) {
      var th = h(thead_tr, "th");
      th.textContent = data[0][j];
    }
    var th = h(thead_tr, "th");
    th.textContent = "Medal";
    var tbody = h(table, "tbody");
    for (var i=1; i<data.length; i++) {
      var tbody_tr = h(tbody, "tr");
      for (var j=0; j<data[i].length; j++) {
        var td = h(tbody_tr, "td");
        td.textContent = data[i][j];
      }
      if (parseInt(data[i][3]) >= 349) {
        tbody_tr.classList.add("medal-gold");
        var td = h(tbody_tr, "td");
        td.textContent = "Gold";
      }else if (parseInt(data[i][3]) >= 290) {
        tbody_tr.classList.add("medal-silver");
        var td = h(tbody_tr, "td");
        td.textContent = "Silver";
      }else if (parseInt(data[i][3]) >= 217) {
        tbody_tr.classList.add("medal-bronze");
        var td = h(tbody_tr, "td");
        td.textContent = "Bronze";
      }else {
        var td = h(tbody_tr, "td");
      }
    }
  }

  httpGetAsync("/open-results.tsv", function(allText) {
    data = processCSV(allText);
    populateCountries();
    populateFilter();
    populateTable(table_el, data);
  });
</script>