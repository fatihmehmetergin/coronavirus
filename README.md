# coronavirus
!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<link rel="apple-touch-icon" type="image/png" href="https://static.codepen.io/assets/favicon/apple-touch-icon-5ae1a0698dcc2402e9712f7d01ed509a57814f994c660df9f7a952f3060705ee.png" />
<meta name="apple-mobile-web-app-title" content="CodePen">
<link rel="shortcut icon" type="image/x-icon" href="https://static.codepen.io/assets/favicon/favicon-aec34940fbc1a6e787974dcd360f2c6b63348d4b1f4e06c77743096d55480f33.ico" />
<link rel="mask-icon" type="" href="https://static.codepen.io/assets/favicon/logo-pin-8f3771b1072e3c38bd662872f6b673a722f4b3ca2421637d5596661b4e2132cc.svg" color="#111" />
<meta charset="utf-8">
<meta name='viewport' content='width=device-width, initial-scale=1'>
<title>CodePen - Pure JavaScript Sortable Table</title>
<link rel="stylesheet" media="screen" href="https://static.codepen.io/assets/fullpage/fullpage-4de243a40619a967c0bf13b95e1ac6f8de89d943b7fc8710de33f681fe287604.css" />
<link href='https://fonts.googleapis.com/css?family=Lato:300,400,400italic,700,700italic,900,900italic' rel='stylesheet'>
<link rel="apple-touch-icon" type="image/png" href="https://static.codepen.io/assets/favicon/apple-touch-icon-5ae1a0698dcc2402e9712f7d01ed509a57814f994c660df9f7a952f3060705ee.png" />
<meta name="apple-mobile-web-app-title" content="CodePen">
<link rel="shortcut icon" type="image/x-icon" href="https://static.codepen.io/assets/favicon/favicon-aec34940fbc1a6e787974dcd360f2c6b63348d4b1f4e06c77743096d55480f33.ico" />
<link rel="mask-icon" type="" href="https://static.codepen.io/assets/favicon/logo-pin-8f3771b1072e3c38bd662872f6b673a722f4b3ca2421637d5596661b4e2132cc.svg" color="#111" />
<title>CodePen - Pure JavaScript Sortable Table</title>
<script>
  if (document.location.search.match(/type=embed/gi)) {
    window.parent.postMessage("resize", "*");
  }
</script>
<style>
    html { font-size: 15px; }
    html, body { margin: 0; padding: 0; min-height: 100%; }
    body { height:100%; display: flex; flex-direction: column; }
    .referer-warning {
      background: black;
      box-shadow: 0 2px 5px rgba(0,0,0, 0.5);
      padding: 0.75em;
      color: white;
      text-align: center;
      font-family: 'Lato', 'Lucida Grande', 'Lucida Sans Unicode', Tahoma, Sans-Serif;
      line-height: 1.2;
      font-size: 1rem;
      position: relative;
      z-index: 2;
    }
    .referer-warning h1 { font-size: 1.2rem; margin: 0; }
    .referer-warning a { color: #56bcf9; } /* $linkColorOnBlack */
  </style>
</head>
<body class="">

<div id="result-iframe-wrap" role="main">
<iframe id="result" srcdoc="
<!DOCTYPE html>
<html lang=&quot;en&quot; >
<head>
  <meta charset=&quot;UTF-8&quot;>
  
<link rel=&quot;apple-touch-icon&quot; type=&quot;image/png&quot; href=&quot;https://static.codepen.io/assets/favicon/apple-touch-icon-5ae1a0698dcc2402e9712f7d01ed509a57814f994c660df9f7a952f3060705ee.png&quot; />
<meta name=&quot;apple-mobile-web-app-title&quot; content=&quot;CodePen&quot;>
<link rel=&quot;shortcut icon&quot; type=&quot;image/x-icon&quot; href=&quot;https://static.codepen.io/assets/favicon/favicon-aec34940fbc1a6e787974dcd360f2c6b63348d4b1f4e06c77743096d55480f33.ico&quot; />
<link rel=&quot;mask-icon&quot; type=&quot;&quot; href=&quot;https://static.codepen.io/assets/favicon/logo-pin-8f3771b1072e3c38bd662872f6b673a722f4b3ca2421637d5596661b4e2132cc.svg&quot; color=&quot;#111&quot; />
  <title>CodePen - Pure JavaScript Sortable Table</title>
  
  
  <link rel=&quot;stylesheet&quot; href=&quot;https://cdnjs.cloudflare.com/ajax/libs/meyer-reset/2.0/reset.min.css&quot;>
  <link rel='stylesheet' href='https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.1.0/css/bootstrap.css'>
  
<style>
th[data-filter-value] {
  cursor: pointer;
}
th.active {
  color: red;
}
</style>
  <script>
  window.console = window.console || function(t) {};
</script>
  
  
  <script>
  if (document.location.search.match(/type=embed/gi)) {
    window.parent.postMessage(&quot;resize&quot;, &quot;*&quot;);
  }
</script>
</head>
<body translate=&quot;no&quot; >
  <table id=&quot;squadTable&quot; class=&quot;table table-dark table-striped&quot;>
        <thead>
            <tr>
                
                <th>Ülke</th>                
                <th data-filter-value=&quot;match&quot;>Toplam Vaka</th>
                <th data-filter-value=&quot;goal&quot;>Ölüm Sayısı</th>
                
                
            </tr>
        </thead>
        <tbody>
        </tbody>
    </table>
   
  
  
      <script id=&quot;rendered-js&quot; >
const data = [
{  
  &quot;fullName&quot;: &quot;Türkiye&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 947,
  &quot;goal&quot;: 21,
 
},
{  
  &quot;fullName&quot;: &quot;Çin&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 81054,
  &quot;goal&quot;: 3261,
},
{  
  &quot;fullName&quot;: &quot;İtalya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 59138,
  &quot;goal&quot;: 5476,
 
},
{  
  &quot;fullName&quot;: &quot;Amerika&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 38164,
  &quot;goal&quot;: 396,
 
},
{  
  &quot;fullName&quot;: &quot;İspanya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 28603,
  &quot;goal&quot;: 1756,
  
},
{  
  &quot;fullName&quot;: &quot;Almanya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 24806,
  &quot;goal&quot;: 93,
 
},
{  
  &quot;fullName&quot;: &quot;İran&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 21638,
  &quot;goal&quot;: 1685,
},
{  
  &quot;fullName&quot;: &quot;Fransa&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 14459,
  &quot;goal&quot;: 562,
},
{  
  &quot;fullName&quot;: &quot;Güney Kore&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 8897,
  &quot;goal&quot;: 104,
  
},
{  
  &quot;fullName&quot;: &quot;İsviçre&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 7367,
  &quot;goal&quot;: 98,
},
{  
  &quot;fullName&quot;: &quot;İngiltere&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 5683,
  &quot;goal&quot;: 281,
},
{  
  &quot;fullName&quot;: &quot;Hollanda&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;:4204,
  &quot;goal&quot;: 179,
},
{  
  &quot;fullName&quot;: &quot;Belçika&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 3401,
  &quot;goal&quot;: 75,
  
},
{  
  &quot;fullName&quot;: &quot;Avusturya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 3302,
  &quot;goal&quot;: 16,
 
},
{  
  &quot;fullName&quot;: &quot;Norveç&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 2263,
  &quot;goal&quot;: 7,
  
},
{  
  &quot;fullName&quot;: &quot;İsveç&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 1931,
  &quot;goal&quot;: 21,
},
{  
  &quot;fullName&quot;: &quot;Portekiz&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 1600,
  &quot;goal&quot;: 14,
 
},
{  
  &quot;fullName&quot;: &quot;Kanada&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 1426,
  &quot;goal&quot;: 20,
},
{  
  &quot;fullName&quot;: &quot;Danimarka&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;:1395,
  &quot;goal&quot;: 13,
},
{  
  &quot;fullName&quot;: &quot;Avustralya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 1353,
  &quot;goal&quot;:7,
  
},
{  
  &quot;fullName&quot;: &quot;Malezya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 1306,
  &quot;goal&quot;: 10,
  
},
{  
  &quot;fullName&quot;: &quot;Brezilya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 1209,
  &quot;goal&quot;: 18,
  
},
{  
  &quot;fullName&quot;: &quot;Çekya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 1120,
  &quot;goal&quot;: '-',
},
{  
  &quot;fullName&quot;: &quot;Japonya&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 1086,
  &quot;goal&quot;: 36,
},
{  
  &quot;fullName&quot;: &quot;İsrail&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 945,
  &quot;goal&quot;: 1,
  
},
{  
  &quot;fullName&quot;: &quot;Lüksemburg&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 798,
  &quot;goal&quot;: 8,
  
},
{  
  &quot;fullName&quot;: &quot;Ekvador&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 789,
  &quot;goal&quot;: 14
  
},
{  
  &quot;fullName&quot;: &quot;İrlanda&quot;,
  &quot;dateOfBirth&quot;: &quot;1985-08-06T00:00:00&quot;,
  &quot;match&quot;: 785	,
  &quot;goal&quot;: 3,
  
},
];
let currentFilter = &quot;&quot;,
prevFilter = &quot;&quot;,
orderAsc = true;
const toggleOrder = () => {
  if (currentFilter === prevFilter) {
    orderAsc = !orderAsc;
  } else {
    orderAsc = true;
  }
};
const calcAge = birthDate => {
  let bDate = new Date(birthDate),
  bDateYear = bDate.getUTCFullYear(),
  now = new Date().getFullYear();
  return now - bDateYear;
};
const sortTable = (array, sortKey) => {
  return array.sort((a, b) => {
    let x = a[sortKey],
    y = b[sortKey];
    return orderAsc ? x - y : y - x;
  });
};
const renderTable = tableData => {
  return `${tableData.map(item => {
    if (item.dateOfBirth.length > 2) {
      item.dateOfBirth = calcAge(item.dateOfBirth);
    }
    return (
      `<tr>
                        
                        <td>${item.fullName}</td>                                   
                        <td>${item.match}</td>
                        <td>${item.goal}</td>
                       
                        
                    </tr>`);
  }).join('')}`;
};
const appendTable = (table, destination) => {
  document.querySelector(destination).innerHTML = table;
};
const handleSortClick = () => {
  const filters = document.querySelectorAll('#squadTable th');
  Array.prototype.forEach.call(filters, filter => {
    filter.addEventListener(&quot;click&quot;, () => {
      if (!filter.dataset.filterValue) return false;
      Array.prototype.forEach.call(filters, filter => {
        filter.classList.remove('active');
      });
      filter.classList.add('active');
      currentFilter = filter.dataset.filterValue;
      toggleOrder();
      init();
    });
  });
};
const init = () => {
  let newTableData = sortTable(data, currentFilter),
  tableOutput = renderTable(newTableData);
  appendTable(tableOutput, '#squadTable tbody');
  prevFilter = currentFilter;
};
init();
handleSortClick();
//# sourceURL=pen.js
    </script>
  
  
</body>
</html>
 
" sandbox="allow-forms allow-modals allow-pointer-lock allow-popups allow-presentation allow-same-origin allow-scripts" allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; microphone; midi; payment; vr" allowTransparency="true" allowpaymentrequest="true" allowfullscreen="true" class="result-iframe">
      </iframe>
</div>
</body>
</html>
