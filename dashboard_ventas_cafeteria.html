<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dashboard de Ventas · Cafetería JP</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.4/chart.umd.min.js"></script>
<style>
  :root{
    --bg:#FBF8F3;
    --surface:#FFFFFF;
    --border:#E6DDCC;
    --ink:#2A1B12;
    --ink-soft:#6E5D4E;
    --brown:#6F4E37;
    --brown-dark:#43301F;
    --brown-light:#B99A7D;
    --teal:#2F6B5E;
    --teal-light:#8FBBAF;
    --caramel:#C17F3E;
    --chip-bg:#F1E9DC;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--ink);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.5;
  }
  h1,h2,h3{
    font-family:'Fraunces', serif;
    color:var(--brown-dark);
    margin:0;
  }
  .wrap{max-width:1180px;margin:0 auto;padding:0 24px 64px;}
  header.top{
    padding:36px 24px 20px;
    border-bottom:1px solid var(--border);
    background:linear-gradient(180deg,#FFFFFF 0%, var(--bg) 100%);
  }
  header.top .wrap{padding:0;display:flex;flex-direction:column;gap:6px;}
  header.top h1{font-size:2rem;font-weight:700;letter-spacing:-0.01em;}
  header.top p{margin:0;color:var(--ink-soft);font-size:0.95rem;max-width:640px;}
  .badge-row{display:flex;gap:8px;flex-wrap:wrap;margin-top:10px;}
  .badge{
    font-size:0.78rem;
    color:var(--brown-dark);
    background:var(--chip-bg);
    border:1px solid var(--border);
    padding:4px 10px;
    border-radius:100px;
  }

  section{padding:32px 0 8px;}
  section h2{font-size:1.35rem;font-weight:600;margin-bottom:4px;}
  section > p.section-note{color:var(--ink-soft);font-size:0.9rem;margin-top:2px;margin-bottom:18px;max-width:760px;}

  /* Filtros */
  .filters{
    position:sticky; top:0; z-index:20;
    background:rgba(255,255,255,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--border);
    padding:14px 24px;
  }
  .filters .wrap{padding:0;display:flex;flex-wrap:wrap;gap:18px;align-items:flex-end;}
  .filter-group{display:flex;flex-direction:column;gap:6px;}
  .filter-group label.title{font-size:0.72rem;text-transform:none;color:var(--ink-soft);font-weight:600;}
  .date-inputs{display:flex;gap:8px;align-items:center;}
  input[type=date]{
    font-family:'IBM Plex Sans',sans-serif;
    border:1px solid var(--border);
    border-radius:8px;
    padding:6px 8px;
    font-size:0.85rem;
    color:var(--ink);
    background:#fff;
  }
  .chip-set{display:flex;gap:6px;flex-wrap:wrap;}
  .chip{
    border:1px solid var(--border);
    background:#fff;
    color:var(--ink-soft);
    padding:6px 12px;
    border-radius:100px;
    font-size:0.82rem;
    cursor:pointer;
    transition:all .15s ease;
    user-select:none;
  }
  .chip:hover{border-color:var(--brown-light);}
  .chip.active{
    background:var(--brown);
    border-color:var(--brown);
    color:#fff;
  }
  details.prod-panel{position:relative;}
  details.prod-panel summary{
    list-style:none;
    cursor:pointer;
    border:1px solid var(--border);
    background:#fff;
    padding:6px 12px;
    border-radius:8px;
    font-size:0.82rem;
    color:var(--ink);
    display:flex;
    align-items:center;
    gap:6px;
  }
  details.prod-panel summary::-webkit-details-marker{display:none;}
  details.prod-panel[open] summary{border-color:var(--brown);}
  .prod-menu{
    position:absolute;
    top:calc(100% + 6px);
    left:0;
    background:#fff;
    border:1px solid var(--border);
    border-radius:10px;
    padding:10px;
    width:260px;
    max-height:260px;
    overflow-y:auto;
    box-shadow:0 8px 24px rgba(42,27,18,0.12);
    display:grid;
    grid-template-columns:1fr;
    gap:4px;
  }
  .prod-menu label{
    display:flex;align-items:center;gap:8px;
    font-size:0.82rem;color:var(--ink);
    padding:3px 4px;border-radius:6px;
  }
  .prod-menu label:hover{background:var(--chip-bg);}
  .prod-actions{display:flex;gap:8px;margin-bottom:6px;}
  .link-btn{
    background:none;border:none;color:var(--teal);font-size:0.76rem;
    cursor:pointer;padding:0;text-decoration:underline;
  }
  .reset-btn{
    border:1px solid var(--border);
    background:#fff;
    color:var(--brown-dark);
    padding:7px 14px;
    border-radius:8px;
    font-size:0.82rem;
    cursor:pointer;
  }
  .reset-btn:hover{border-color:var(--brown);}

  /* KPI cards */
  .kpi-grid{
    display:grid;
    grid-template-columns:repeat(5,1fr);
    gap:14px;
  }
  .kpi-card{
    background:var(--surface);
    border:1px solid var(--border);
    border-radius:14px;
    padding:18px 18px;
  }
  .kpi-card .label{font-size:0.78rem;color:var(--ink-soft);font-weight:500;}
  .kpi-card .value{
    font-family:'Fraunces',serif;
    font-size:1.9rem;
    font-weight:600;
    color:var(--brown-dark);
    margin-top:4px;
    line-height:1.1;
  }
  .kpi-card .sub{font-size:0.74rem;color:var(--ink-soft);margin-top:4px;}

  /* Charts grid */
  .chart-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:18px;
  }
  .chart-card{
    background:var(--surface);
    border:1px solid var(--border);
    border-radius:14px;
    padding:18px 20px 12px;
  }
  .chart-card h3{font-size:1rem;font-weight:600;margin-bottom:2px;}
  .chart-card .desc{font-size:0.8rem;color:var(--ink-soft);margin-bottom:10px;}
  .chart-card .canvas-wrap{position:relative;height:260px;}
  .chart-card.wide{grid-column:1 / -1;}
  .empty-msg{
    color:var(--ink-soft);
    font-size:0.85rem;
    text-align:center;
    padding:40px 0;
  }

  /* Tables */
  table.data-table{
    width:100%;
    border-collapse:collapse;
    font-size:0.82rem;
  }
  table.data-table th,table.data-table td{
    padding:8px 10px;
    text-align:center;
    border-bottom:1px solid var(--border);
  }
  table.data-table th{
    color:var(--ink-soft);
    font-weight:600;
    font-size:0.74rem;
    text-transform:uppercase;
    letter-spacing:0.03em;
  }
  table.data-table td.prod-name, table.data-table th.prod-name{
    text-align:left;
    font-weight:500;
    color:var(--ink);
  }
  table.clients td, table.clients th{text-align:left;}
  table.clients td:nth-child(2),table.clients td:nth-child(3),table.clients td:nth-child(4),
  table.clients th:nth-child(2),table.clients th:nth-child(3),table.clients th:nth-child(4){text-align:right;}

  footer.notes{
    padding:28px 0 60px;
    border-top:1px solid var(--border);
    margin-top:20px;
    color:var(--ink-soft);
    font-size:0.82rem;
  }
  footer.notes h3{font-size:0.95rem;color:var(--brown-dark);margin-bottom:8px;}
  footer.notes ul{margin:0;padding-left:18px;}
  footer.notes li{margin-bottom:5px;}

  @media (max-width:920px){
    .kpi-grid{grid-template-columns:repeat(2,1fr);}
    .chart-grid{grid-template-columns:1fr;}
  }
</style>
</head>
<body>

<header class="top">
  <div class="wrap">
    <h1>Dashboard de ventas — Cafetería JP</h1>
    <p>Registro de ventas del 1 al 21 de octubre de 2025 (50 transacciones, 27 clientes). Usa los filtros para explorar por fecha, categoría, producto y género.</p>
    <div class="badge-row">
      <span class="badge">50 ventas registradas</span>
      <span class="badge">18 días con actividad de 21</span>
      <span class="badge">27 clientes únicos</span>
      <span class="badge">CDMX</span>
    </div>
  </div>
</header>

<div class="filters">
  <div class="wrap">
    <div class="filter-group">
      <label class="title">Rango de fechas</label>
      <div class="date-inputs">
        <input type="date" id="dateFrom" min="2025-10-01" max="2025-10-21" value="2025-10-01">
        <span style="color:var(--ink-soft);">–</span>
        <input type="date" id="dateTo" min="2025-10-01" max="2025-10-21" value="2025-10-21">
      </div>
    </div>
    <div class="filter-group">
      <label class="title">Categoría</label>
      <div class="chip-set" id="catChips"></div>
    </div>
    <div class="filter-group">
      <label class="title">Género</label>
      <div class="chip-set" id="genChips"></div>
    </div>
    <div class="filter-group">
      <label class="title">Producto</label>
      <details class="prod-panel" id="prodPanel">
        <summary id="prodSummary">Todos los productos ▾</summary>
        <div class="prod-menu">
          <div class="prod-actions">
            <button class="link-btn" id="prodAll">Seleccionar todos</button>
            <button class="link-btn" id="prodNone">Limpiar</button>
          </div>
          <div id="prodList"></div>
        </div>
      </details>
    </div>
    <div class="filter-group">
      <label class="title">&nbsp;</label>
      <button class="reset-btn" id="resetBtn">Reiniciar filtros</button>
    </div>
  </div>
</div>

<div class="wrap">

  <section id="kpis">
    <h2>Indicadores clave</h2>
    <p class="section-note">Se recalculan según los filtros activos.</p>
    <div class="kpi-grid">
      <div class="kpi-card"><div class="label">Ventas totales</div><div class="value" id="kpiVentas">—</div><div class="sub" id="kpiVentasSub"></div></div>
      <div class="kpi-card"><div class="label">Pedidos</div><div class="value" id="kpiPedidos">—</div><div class="sub">transacciones registradas</div></div>
      <div class="kpi-card"><div class="label">Ticket promedio</div><div class="value" id="kpiTicket">—</div><div class="sub">por pedido</div></div>
      <div class="kpi-card"><div class="label">Clientes únicos</div><div class="value" id="kpiClientes">—</div><div class="sub" id="kpiClientesSub"></div></div>
      <div class="kpi-card"><div class="label">Unidades vendidas</div><div class="value" id="kpiUnidades">—</div><div class="sub">piezas / bebidas</div></div>
    </div>
  </section>

  <section id="charts">
    <h2>Gráficos principales</h2>
    <p class="section-note">Ticket promedio y margen por producto: no disponibles en los datos proporcionados (no se incluyen costos).</p>
    <div class="chart-grid">

      <div class="chart-card wide">
        <h3>Evolución de ventas por día</h3>
        <div class="desc">Ingresos totales ($) por fecha. Los días sin barra no tuvieron ventas registradas.</div>
        <div class="canvas-wrap"><canvas id="chartDaily"></canvas></div>
      </div>

      <div class="chart-card">
        <h3>Ventas por producto</h3>
        <div class="desc">Ingresos totales por producto, de mayor a menor.</div>
        <div class="canvas-wrap"><canvas id="chartProduct"></canvas></div>
      </div>

      <div class="chart-card">
        <h3>Ventas por canal</h3>
        <div class="desc">Ingresos por canal de venta.</div>
        <div class="canvas-wrap"><canvas id="chartChannel"></canvas></div>
      </div>

      <div class="chart-card">
        <h3>Ventas por turno</h3>
        <div class="desc">Ingresos según franja horaria de la venta.</div>
        <div class="canvas-wrap"><canvas id="chartShift"></canvas></div>
      </div>

      <div class="chart-card">
        <h3>Categoría según género</h3>
        <div class="desc">Perfil del comprador: ingresos por categoría, separados por género.</div>
        <div class="canvas-wrap"><canvas id="chartGenderCat"></canvas></div>
      </div>

      <div class="chart-card wide">
        <h3>Clientes nuevos vs. recurrentes</h3>
        <div class="desc">Ingresos y número de pedidos según si el cliente era nuevo o ya había comprado antes.</div>
        <div class="canvas-wrap" style="height:220px;"><canvas id="chartNewReturning"></canvas></div>
      </div>

    </div>
  </section>

  <section id="cross">
    <h2>Análisis cruzado: producto × día de la semana</h2>
    <p class="section-note">Mapa de calor de ingresos ($). Color más intenso = mayor ingreso en esa combinación producto–día, dentro del rango filtrado.</p>
    <div class="chart-card wide" style="overflow-x:auto;">
      <div id="heatmapWrap"></div>
      <div class="empty-msg" id="heatmapEmpty" style="display:none;">No hay ventas para esta combinación de filtros.</div>
    </div>
  </section>

  <section id="clients">
    <h2>Clientes más recurrentes</h2>
    <p class="section-note">Clientes con más de una compra en el periodo filtrado, ordenados por ingreso generado.</p>
    <div class="chart-card wide" style="overflow-x:auto;">
      <table class="data-table clients" id="clientsTable">
        <thead><tr><th>Cliente</th><th>Compras</th><th>Ingreso total</th><th>Ticket promedio</th><th>Zona más frecuente</th></tr></thead>
        <tbody></tbody>
      </table>
      <div class="empty-msg" id="clientsEmpty" style="display:none;">No hay clientes recurrentes en esta selección.</div>
    </div>
  </section>

  <footer class="notes">
    <h3>Notas sobre los datos</h3>
    <ul>
      <li>Fuente: archivo <em>ventas_cafeteria_JP</em> (idéntico en formato PDF y XLSX), 50 registros, 20 columnas, sin valores nulos.</li>
      <li>El campo "descuento" es un monto en pesos (no un porcentaje): total = precio unitario × cantidad − descuento. Se verificó en el 100% de los registros.</li>
      <li>Todas las ventas ocurren en una sola ciudad (CDMX), por lo que "ciudad" no se usa como filtro; se usa "zona" (Centro, Norte, Sur, Oriente, Poniente) para la segmentación geográfica.</li>
      <li>No hay datos de costos, por lo que el margen no es calculable ("No disponible en los datos proporcionados").</li>
      <li>Muestra pequeña (50 ventas / 27 clientes en 21 días): los porcentajes deben leerse como tendencias observadas en este periodo, no como conclusiones estadísticamente robustas.</li>
    </ul>
  </footer>

</div>

<script id="sales-data" type="application/json">[{"venta_id": "V001", "fecha": "2025-10-21", "dia_semana": "Tuesday", "hora": "7:00", "turno": "Mañana", "categoria": "Postres", "producto": "Cheesecake", "precio_unitario": 90, "cantidad": 1, "descuento": 0, "total": 90, "canal": "WhatsApp", "origen": "Recomendación", "metodo_pago": "Tarjeta", "edad": 32, "genero": "Mujer", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C019", "cliente_nuevo": "Sí"}, {"venta_id": "V002", "fecha": "2025-10-10", "dia_semana": "Friday", "hora": "21:50", "turno": "Noche", "categoria": "Postres", "producto": "Pastel de zanahoria", "precio_unitario": 85, "cantidad": 1, "descuento": 10, "total": 75, "canal": "App Delivery", "origen": "Recomendación", "metodo_pago": "Tarjeta", "edad": 60, "genero": "Hombre", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C023", "cliente_nuevo": "Sí"}, {"venta_id": "V003", "fecha": "2025-10-04", "dia_semana": "Saturday", "hora": "7:50", "turno": "Mañana", "categoria": "Alimentos", "producto": "Sandwich integral", "precio_unitario": 80, "cantidad": 1, "descuento": 10, "total": 70, "canal": "App Delivery", "origen": "Anuncio", "metodo_pago": "Tarjeta", "edad": 32, "genero": "Mujer", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C009", "cliente_nuevo": "No"}, {"venta_id": "V004", "fecha": "2025-10-16", "dia_semana": "Thursday", "hora": "10:20", "turno": "Mañana", "categoria": "Alimentos", "producto": "Sandwich integral", "precio_unitario": 80, "cantidad": 2, "descuento": 15, "total": 145, "canal": "Mostrador", "origen": "Recomendación", "metodo_pago": "Tarjeta", "edad": 53, "genero": "Mujer", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C015", "cliente_nuevo": "No"}, {"venta_id": "V005", "fecha": "2025-10-19", "dia_semana": "Sunday", "hora": "16:30", "turno": "Tarde", "categoria": "Postres", "producto": "Cheesecake", "precio_unitario": 90, "cantidad": 3, "descuento": 10, "total": 260, "canal": "WhatsApp", "origen": "Promoción", "metodo_pago": "Efectivo", "edad": 44, "genero": "Hombre", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C019", "cliente_nuevo": "Sí"}, {"venta_id": "V006", "fecha": "2025-10-01", "dia_semana": "Wednesday", "hora": "19:10", "turno": "Noche", "categoria": "Postres", "producto": "Pastel de zanahoria", "precio_unitario": 85, "cantidad": 1, "descuento": 0, "total": 85, "canal": "WhatsApp", "origen": "Orgánico", "metodo_pago": "Transferencia", "edad": 45, "genero": "Mujer", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C026", "cliente_nuevo": "Sí"}, {"venta_id": "V007", "fecha": "2025-10-17", "dia_semana": "Friday", "hora": "7:50", "turno": "Mañana", "categoria": "Bebidas", "producto": "Cappuccino", "precio_unitario": 65, "cantidad": 3, "descuento": 0, "total": 195, "canal": "App Delivery", "origen": "Orgánico", "metodo_pago": "Tarjeta", "edad": 33, "genero": "Mujer", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C027", "cliente_nuevo": "Sí"}, {"venta_id": "V008", "fecha": "2025-10-04", "dia_semana": "Saturday", "hora": "7:10", "turno": "Mañana", "categoria": "Bebidas", "producto": "Cappuccino", "precio_unitario": 65, "cantidad": 2, "descuento": 15, "total": 115, "canal": "App Delivery", "origen": "Orgánico", "metodo_pago": "Tarjeta", "edad": 58, "genero": "Hombre", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C008", "cliente_nuevo": "No"}, {"venta_id": "V009", "fecha": "2025-10-06", "dia_semana": "Monday", "hora": "12:15", "turno": "Tarde", "categoria": "Bebidas", "producto": "Café Americano", "precio_unitario": 45, "cantidad": 2, "descuento": 0, "total": 90, "canal": "Mostrador", "origen": "Promoción", "metodo_pago": "Tarjeta", "edad": 46, "genero": "Mujer", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C018", "cliente_nuevo": "No"}, {"venta_id": "V010", "fecha": "2025-10-17", "dia_semana": "Friday", "hora": "8:10", "turno": "Mañana", "categoria": "Postres", "producto": "Pastel de zanahoria", "precio_unitario": 85, "cantidad": 3, "descuento": 10, "total": 245, "canal": "Instagram", "origen": "Orgánico", "metodo_pago": "Transferencia", "edad": 44, "genero": "Hombre", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C020", "cliente_nuevo": "No"}, {"venta_id": "V011", "fecha": "2025-10-05", "dia_semana": "Sunday", "hora": "11:40", "turno": "Mañana", "categoria": "Bebidas", "producto": "Cappuccino", "precio_unitario": 65, "cantidad": 2, "descuento": 0, "total": 130, "canal": "App Delivery", "origen": "Orgánico", "metodo_pago": "Tarjeta", "edad": 50, "genero": "Hombre", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C028", "cliente_nuevo": "No"}, {"venta_id": "V012", "fecha": "2025-10-19", "dia_semana": "Sunday", "hora": "19:10", "turno": "Noche", "categoria": "Bebidas", "producto": "Chocolate Caliente", "precio_unitario": 60, "cantidad": 3, "descuento": 0, "total": 180, "canal": "App Delivery", "origen": "Orgánico", "metodo_pago": "Tarjeta", "edad": 34, "genero": "Hombre", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C025", "cliente_nuevo": "Sí"}, {"venta_id": "V013", "fecha": "2025-10-21", "dia_semana": "Tuesday", "hora": "13:40", "turno": "Tarde", "categoria": "Alimentos", "producto": "Sandwich integral", "precio_unitario": 80, "cantidad": 1, "descuento": 0, "total": 80, "canal": "App Delivery", "origen": "Orgánico", "metodo_pago": "Efectivo", "edad": 55, "genero": "Mujer", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C007", "cliente_nuevo": "No"}, {"venta_id": "V014", "fecha": "2025-10-06", "dia_semana": "Monday", "hora": "10:20", "turno": "Mañana", "categoria": "Bebidas", "producto": "Café Americano", "precio_unitario": 45, "cantidad": 1, "descuento": 15, "total": 30, "canal": "Mostrador", "origen": "Recomendación", "metodo_pago": "Efectivo", "edad": 38, "genero": "Mujer", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C002", "cliente_nuevo": "Sí"}, {"venta_id": "V015", "fecha": "2025-10-05", "dia_semana": "Sunday", "hora": "18:40", "turno": "Noche", "categoria": "Alimentos", "producto": "Panini", "precio_unitario": 95, "cantidad": 1, "descuento": 15, "total": 80, "canal": "WhatsApp", "origen": "Promoción", "metodo_pago": "Tarjeta", "edad": 46, "genero": "Mujer", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C013", "cliente_nuevo": "No"}, {"venta_id": "V016", "fecha": "2025-10-13", "dia_semana": "Monday", "hora": "17:00", "turno": "Tarde", "categoria": "Postres", "producto": "Cheesecake", "precio_unitario": 90, "cantidad": 2, "descuento": 0, "total": 180, "canal": "WhatsApp", "origen": "Promoción", "metodo_pago": "Transferencia", "edad": 28, "genero": "Mujer", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C005", "cliente_nuevo": "Sí"}, {"venta_id": "V017", "fecha": "2025-10-21", "dia_semana": "Tuesday", "hora": "20:20", "turno": "Noche", "categoria": "Alimentos", "producto": "Sandwich integral", "precio_unitario": 80, "cantidad": 2, "descuento": 0, "total": 160, "canal": "Instagram", "origen": "Promoción", "metodo_pago": "Tarjeta", "edad": 58, "genero": "Mujer", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C019", "cliente_nuevo": "No"}, {"venta_id": "V018", "fecha": "2025-10-21", "dia_semana": "Tuesday", "hora": "11:10", "turno": "Mañana", "categoria": "Alimentos", "producto": "Panini", "precio_unitario": 95, "cantidad": 3, "descuento": 0, "total": 285, "canal": "Instagram", "origen": "Orgánico", "metodo_pago": "Transferencia", "edad": 36, "genero": "Hombre", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C002", "cliente_nuevo": "No"}, {"venta_id": "V019", "fecha": "2025-10-16", "dia_semana": "Thursday", "hora": "17:40", "turno": "Tarde", "categoria": "Postres", "producto": "Pastel de zanahoria", "precio_unitario": 85, "cantidad": 3, "descuento": 0, "total": 255, "canal": "WhatsApp", "origen": "Promoción", "metodo_pago": "Transferencia", "edad": 54, "genero": "Hombre", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C007", "cliente_nuevo": "Sí"}, {"venta_id": "V020", "fecha": "2025-10-04", "dia_semana": "Saturday", "hora": "21:40", "turno": "Noche", "categoria": "Bebidas", "producto": "Frappé", "precio_unitario": 85, "cantidad": 3, "descuento": 10, "total": 245, "canal": "Instagram", "origen": "Promoción", "metodo_pago": "Tarjeta", "edad": 25, "genero": "Hombre", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C015", "cliente_nuevo": "Sí"}, {"venta_id": "V021", "fecha": "2025-10-18", "dia_semana": "Saturday", "hora": "14:50", "turno": "Tarde", "categoria": "Alimentos", "producto": "Muffin de arándano", "precio_unitario": 50, "cantidad": 3, "descuento": 15, "total": 135, "canal": "WhatsApp", "origen": "Recomendación", "metodo_pago": "Tarjeta", "edad": 37, "genero": "Mujer", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C021", "cliente_nuevo": "No"}, {"venta_id": "V022", "fecha": "2025-10-07", "dia_semana": "Tuesday", "hora": "19:20", "turno": "Noche", "categoria": "Postres", "producto": "Galleta artesanal", "precio_unitario": 35, "cantidad": 1, "descuento": 10, "total": 25, "canal": "WhatsApp", "origen": "Recomendación", "metodo_pago": "Efectivo", "edad": 30, "genero": "Mujer", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C001", "cliente_nuevo": "Sí"}, {"venta_id": "V023", "fecha": "2025-10-08", "dia_semana": "Wednesday", "hora": "21:20", "turno": "Noche", "categoria": "Alimentos", "producto": "Bagel con queso crema", "precio_unitario": 55, "cantidad": 1, "descuento": 0, "total": 55, "canal": "Mostrador", "origen": "Anuncio", "metodo_pago": "Transferencia", "edad": 24, "genero": "Hombre", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C006", "cliente_nuevo": "No"}, {"venta_id": "V024", "fecha": "2025-10-04", "dia_semana": "Saturday", "hora": "7:50", "turno": "Mañana", "categoria": "Alimentos", "producto": "Muffin de arándano", "precio_unitario": 50, "cantidad": 3, "descuento": 0, "total": 150, "canal": "Mostrador", "origen": "Orgánico", "metodo_pago": "Tarjeta", "edad": 47, "genero": "Mujer", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C004", "cliente_nuevo": "No"}, {"venta_id": "V025", "fecha": "2025-10-16", "dia_semana": "Thursday", "hora": "13:50", "turno": "Tarde", "categoria": "Alimentos", "producto": "Muffin de arándano", "precio_unitario": 50, "cantidad": 2, "descuento": 10, "total": 90, "canal": "App Delivery", "origen": "Promoción", "metodo_pago": "Transferencia", "edad": 51, "genero": "Hombre", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C027", "cliente_nuevo": "Sí"}, {"venta_id": "V026", "fecha": "2025-10-11", "dia_semana": "Saturday", "hora": "20:50", "turno": "Noche", "categoria": "Postres", "producto": "Brownie", "precio_unitario": 55, "cantidad": 1, "descuento": 0, "total": 55, "canal": "WhatsApp", "origen": "Recomendación", "metodo_pago": "Efectivo", "edad": 31, "genero": "Mujer", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C024", "cliente_nuevo": "No"}, {"venta_id": "V027", "fecha": "2025-10-10", "dia_semana": "Friday", "hora": "14:10", "turno": "Tarde", "categoria": "Alimentos", "producto": "Sandwich integral", "precio_unitario": 80, "cantidad": 2, "descuento": 15, "total": 145, "canal": "WhatsApp", "origen": "Anuncio", "metodo_pago": "Efectivo", "edad": 24, "genero": "Mujer", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C019", "cliente_nuevo": "No"}, {"venta_id": "V028", "fecha": "2025-10-05", "dia_semana": "Sunday", "hora": "19:50", "turno": "Noche", "categoria": "Bebidas", "producto": "Cappuccino", "precio_unitario": 65, "cantidad": 2, "descuento": 0, "total": 130, "canal": "Mostrador", "origen": "Promoción", "metodo_pago": "Tarjeta", "edad": 45, "genero": "Hombre", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C013", "cliente_nuevo": "No"}, {"venta_id": "V029", "fecha": "2025-10-09", "dia_semana": "Thursday", "hora": "20:50", "turno": "Noche", "categoria": "Alimentos", "producto": "Muffin de arándano", "precio_unitario": 50, "cantidad": 1, "descuento": 10, "total": 40, "canal": "WhatsApp", "origen": "Promoción", "metodo_pago": "Tarjeta", "edad": 20, "genero": "Mujer", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C029", "cliente_nuevo": "Sí"}, {"venta_id": "V030", "fecha": "2025-10-19", "dia_semana": "Sunday", "hora": "21:45", "turno": "Noche", "categoria": "Bebidas", "producto": "Chocolate Caliente", "precio_unitario": 60, "cantidad": 1, "descuento": 15, "total": 45, "canal": "Mostrador", "origen": "Orgánico", "metodo_pago": "Tarjeta", "edad": 29, "genero": "Mujer", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C004", "cliente_nuevo": "Sí"}, {"venta_id": "V031", "fecha": "2025-10-01", "dia_semana": "Wednesday", "hora": "8:30", "turno": "Mañana", "categoria": "Bebidas", "producto": "Café Americano", "precio_unitario": 45, "cantidad": 1, "descuento": 0, "total": 45, "canal": "Mostrador", "origen": "Recomendación", "metodo_pago": "Tarjeta", "edad": 27, "genero": "Mujer", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C025", "cliente_nuevo": "Sí"}, {"venta_id": "V032", "fecha": "2025-10-02", "dia_semana": "Thursday", "hora": "14:20", "turno": "Tarde", "categoria": "Alimentos", "producto": "Panini", "precio_unitario": 95, "cantidad": 2, "descuento": 10, "total": 180, "canal": "App Delivery", "origen": "Recomendación", "metodo_pago": "Transferencia", "edad": 36, "genero": "Hombre", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C007", "cliente_nuevo": "Sí"}, {"venta_id": "V033", "fecha": "2025-10-18", "dia_semana": "Saturday", "hora": "20:20", "turno": "Noche", "categoria": "Alimentos", "producto": "Croissant", "precio_unitario": 40, "cantidad": 2, "descuento": 15, "total": 65, "canal": "Mostrador", "origen": "Anuncio", "metodo_pago": "Tarjeta", "edad": 22, "genero": "Hombre", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C003", "cliente_nuevo": "Sí"}, {"venta_id": "V034", "fecha": "2025-10-11", "dia_semana": "Saturday", "hora": "17:15", "turno": "Tarde", "categoria": "Postres", "producto": "Galleta artesanal", "precio_unitario": 35, "cantidad": 2, "descuento": 0, "total": 70, "canal": "Mostrador", "origen": "Orgánico", "metodo_pago": "Tarjeta", "edad": 29, "genero": "Mujer", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C030", "cliente_nuevo": "No"}, {"venta_id": "V035", "fecha": "2025-10-11", "dia_semana": "Saturday", "hora": "12:20", "turno": "Tarde", "categoria": "Bebidas", "producto": "Café Americano", "precio_unitario": 45, "cantidad": 1, "descuento": 10, "total": 35, "canal": "Mostrador", "origen": "Promoción", "metodo_pago": "Efectivo", "edad": 20, "genero": "Hombre", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C021", "cliente_nuevo": "Sí"}, {"venta_id": "V036", "fecha": "2025-10-08", "dia_semana": "Wednesday", "hora": "17:10", "turno": "Tarde", "categoria": "Alimentos", "producto": "Muffin de arándano", "precio_unitario": 50, "cantidad": 2, "descuento": 10, "total": 90, "canal": "WhatsApp", "origen": "Anuncio", "metodo_pago": "Tarjeta", "edad": 25, "genero": "Mujer", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C023", "cliente_nuevo": "No"}, {"venta_id": "V037", "fecha": "2025-10-04", "dia_semana": "Saturday", "hora": "19:00", "turno": "Noche", "categoria": "Postres", "producto": "Galleta artesanal", "precio_unitario": 35, "cantidad": 1, "descuento": 0, "total": 35, "canal": "Mostrador", "origen": "Anuncio", "metodo_pago": "Tarjeta", "edad": 50, "genero": "Mujer", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C020", "cliente_nuevo": "Sí"}, {"venta_id": "V038", "fecha": "2025-10-08", "dia_semana": "Wednesday", "hora": "9:10", "turno": "Mañana", "categoria": "Postres", "producto": "Pastel de zanahoria", "precio_unitario": 85, "cantidad": 2, "descuento": 15, "total": 155, "canal": "App Delivery", "origen": "Recomendación", "metodo_pago": "Tarjeta", "edad": 37, "genero": "Hombre", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C009", "cliente_nuevo": "Sí"}, {"venta_id": "V039", "fecha": "2025-10-20", "dia_semana": "Monday", "hora": "19:30", "turno": "Noche", "categoria": "Postres", "producto": "Cheesecake", "precio_unitario": 90, "cantidad": 1, "descuento": 0, "total": 90, "canal": "WhatsApp", "origen": "Promoción", "metodo_pago": "Efectivo", "edad": 22, "genero": "Hombre", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C020", "cliente_nuevo": "Sí"}, {"venta_id": "V040", "fecha": "2025-10-08", "dia_semana": "Wednesday", "hora": "14:50", "turno": "Tarde", "categoria": "Postres", "producto": "Pastel de zanahoria", "precio_unitario": 85, "cantidad": 3, "descuento": 0, "total": 255, "canal": "WhatsApp", "origen": "Orgánico", "metodo_pago": "Efectivo", "edad": 49, "genero": "Hombre", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C013", "cliente_nuevo": "Sí"}, {"venta_id": "V041", "fecha": "2025-10-15", "dia_semana": "Wednesday", "hora": "15:10", "turno": "Tarde", "categoria": "Postres", "producto": "Pastel de zanahoria", "precio_unitario": 85, "cantidad": 1, "descuento": 10, "total": 75, "canal": "Instagram", "origen": "Promoción", "metodo_pago": "Efectivo", "edad": 58, "genero": "Mujer", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C011", "cliente_nuevo": "Sí"}, {"venta_id": "V042", "fecha": "2025-10-15", "dia_semana": "Wednesday", "hora": "15:45", "turno": "Tarde", "categoria": "Alimentos", "producto": "Sandwich integral", "precio_unitario": 80, "cantidad": 1, "descuento": 10, "total": 70, "canal": "WhatsApp", "origen": "Anuncio", "metodo_pago": "Tarjeta", "edad": 26, "genero": "Hombre", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C021", "cliente_nuevo": "No"}, {"venta_id": "V043", "fecha": "2025-10-15", "dia_semana": "Wednesday", "hora": "16:50", "turno": "Tarde", "categoria": "Postres", "producto": "Galleta artesanal", "precio_unitario": 35, "cantidad": 3, "descuento": 15, "total": 90, "canal": "App Delivery", "origen": "Promoción", "metodo_pago": "Efectivo", "edad": 53, "genero": "Hombre", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C021", "cliente_nuevo": "Sí"}, {"venta_id": "V044", "fecha": "2025-10-04", "dia_semana": "Saturday", "hora": "19:20", "turno": "Noche", "categoria": "Postres", "producto": "Cheesecake", "precio_unitario": 90, "cantidad": 2, "descuento": 0, "total": 180, "canal": "Instagram", "origen": "Anuncio", "metodo_pago": "Efectivo", "edad": 41, "genero": "Mujer", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C010", "cliente_nuevo": "Sí"}, {"venta_id": "V045", "fecha": "2025-10-13", "dia_semana": "Monday", "hora": "9:30", "turno": "Mañana", "categoria": "Postres", "producto": "Pastel de zanahoria", "precio_unitario": 85, "cantidad": 3, "descuento": 0, "total": 255, "canal": "Mostrador", "origen": "Anuncio", "metodo_pago": "Tarjeta", "edad": 49, "genero": "Hombre", "ciudad": "CDMX", "zona": "Norte", "cliente_id": "C014", "cliente_nuevo": "Sí"}, {"venta_id": "V046", "fecha": "2025-10-04", "dia_semana": "Saturday", "hora": "14:50", "turno": "Tarde", "categoria": "Alimentos", "producto": "Croissant", "precio_unitario": 40, "cantidad": 2, "descuento": 15, "total": 65, "canal": "Instagram", "origen": "Promoción", "metodo_pago": "Tarjeta", "edad": 37, "genero": "Hombre", "ciudad": "CDMX", "zona": "Centro", "cliente_id": "C004", "cliente_nuevo": "Sí"}, {"venta_id": "V047", "fecha": "2025-10-16", "dia_semana": "Thursday", "hora": "19:40", "turno": "Noche", "categoria": "Alimentos", "producto": "Sandwich integral", "precio_unitario": 80, "cantidad": 1, "descuento": 0, "total": 80, "canal": "WhatsApp", "origen": "Promoción", "metodo_pago": "Efectivo", "edad": 52, "genero": "Hombre", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C019", "cliente_nuevo": "No"}, {"venta_id": "V048", "fecha": "2025-10-08", "dia_semana": "Wednesday", "hora": "15:50", "turno": "Tarde", "categoria": "Postres", "producto": "Galleta artesanal", "precio_unitario": 35, "cantidad": 3, "descuento": 15, "total": 90, "canal": "Instagram", "origen": "Promoción", "metodo_pago": "Tarjeta", "edad": 49, "genero": "Hombre", "ciudad": "CDMX", "zona": "Sur", "cliente_id": "C003", "cliente_nuevo": "No"}, {"venta_id": "V049", "fecha": "2025-10-21", "dia_semana": "Tuesday", "hora": "21:30", "turno": "Noche", "categoria": "Alimentos", "producto": "Croissant", "precio_unitario": 40, "cantidad": 2, "descuento": 0, "total": 80, "canal": "Mostrador", "origen": "Recomendación", "metodo_pago": "Tarjeta", "edad": 50, "genero": "Mujer", "ciudad": "CDMX", "zona": "Oriente", "cliente_id": "C030", "cliente_nuevo": "Sí"}, {"venta_id": "V050", "fecha": "2025-10-08", "dia_semana": "Wednesday", "hora": "20:00", "turno": "Noche", "categoria": "Alimentos", "producto": "Croissant", "precio_unitario": 40, "cantidad": 1, "descuento": 0, "total": 40, "canal": "Mostrador", "origen": "Recomendación", "metodo_pago": "Transferencia", "edad": 22, "genero": "Mujer", "ciudad": "CDMX", "zona": "Poniente", "cliente_id": "C022", "cliente_nuevo": "No"}]</script>
<script>
const RAW = JSON.parse(document.getElementById('sales-data').textContent);

const DAY_ES = {Monday:'Lunes',Tuesday:'Martes',Wednesday:'Miércoles',Thursday:'Jueves',Friday:'Viernes',Saturday:'Sábado',Sunday:'Domingo'};
const DAY_ORDER = ['Monday','Tuesday','Wednesday','Thursday','Friday','Saturday','Sunday'];
const SHIFT_ORDER = ['Mañana','Tarde','Noche'];
const CATS = [...new Set(RAW.map(r=>r.categoria))];
const GENS = [...new Set(RAW.map(r=>r.genero))];
const PRODUCTS = [...new Set(RAW.map(r=>r.producto))].sort();

const money = (n) => new Intl.NumberFormat('es-MX',{style:'currency',currency:'MXN',maximumFractionDigits:0}).format(n);

// ---- filter state ----
const state = {
  from: '2025-10-01',
  to: '2025-10-21',
  cats: new Set(CATS),
  gens: new Set(GENS),
  prods: new Set(PRODUCTS),
};

// ---- build chip / checkbox UI ----
function buildChips(containerId, values, selectedSet, allLabel){
  const el = document.getElementById(containerId);
  el.innerHTML = '';
  const allChip = document.createElement('div');
  allChip.className = 'chip active';
  allChip.textContent = allLabel;
  allChip.dataset.all = '1';
  el.appendChild(allChip);
  values.forEach(v=>{
    const chip = document.createElement('div');
    chip.className = 'chip active';
    chip.textContent = v;
    chip.dataset.value = v;
    el.appendChild(chip);
  });
  el.addEventListener('click', (e)=>{
    const t = e.target;
    if(!t.classList.contains('chip')) return;
    if(t.dataset.all){
      selectedSet.clear();
      values.forEach(v=>selectedSet.add(v));
      [...el.children].forEach(c=>c.classList.add('active'));
    } else {
      const v = t.dataset.value;
      if(selectedSet.has(v)){ selectedSet.delete(v); t.classList.remove('active'); }
      else { selectedSet.add(v); t.classList.add('active'); }
      const allSelected = values.every(v=>selectedSet.has(v));
      el.querySelector('[data-all]').classList.toggle('active', allSelected);
    }
    renderAll();
  });
}
buildChips('catChips', CATS, state.cats, 'Todas');
buildChips('genChips', GENS, state.gens, 'Todos');

function buildProductList(){
  const list = document.getElementById('prodList');
  list.innerHTML = '';
  PRODUCTS.forEach(p=>{
    const label = document.createElement('label');
    const cb = document.createElement('input');
    cb.type = 'checkbox';
    cb.checked = true;
    cb.value = p;
    cb.addEventListener('change', ()=>{
      if(cb.checked) state.prods.add(p); else state.prods.delete(p);
      updateProdSummary();
      renderAll();
    });
    label.appendChild(cb);
    label.appendChild(document.createTextNode(p));
    list.appendChild(label);
  });
}
buildProductList();
document.getElementById('prodAll').addEventListener('click', ()=>{
  state.prods = new Set(PRODUCTS);
  document.querySelectorAll('#prodList input').forEach(cb=>cb.checked=true);
  updateProdSummary(); renderAll();
});
document.getElementById('prodNone').addEventListener('click', ()=>{
  state.prods.clear();
  document.querySelectorAll('#prodList input').forEach(cb=>cb.checked=false);
  updateProdSummary(); renderAll();
});
function updateProdSummary(){
  const n = state.prods.size;
  document.getElementById('prodSummary').textContent =
    (n===PRODUCTS.length ? 'Todos los productos' : n===0 ? 'Ningún producto' : n + ' productos seleccionados') + ' ▾';
}

document.getElementById('dateFrom').addEventListener('change', e=>{ state.from = e.target.value; renderAll(); });
document.getElementById('dateTo').addEventListener('change', e=>{ state.to = e.target.value; renderAll(); });
document.getElementById('resetBtn').addEventListener('click', ()=>{
  state.from='2025-10-01'; state.to='2025-10-21';
  state.cats = new Set(CATS); state.gens = new Set(GENS); state.prods = new Set(PRODUCTS);
  document.getElementById('dateFrom').value = state.from;
  document.getElementById('dateTo').value = state.to;
  buildChips('catChips', CATS, state.cats, 'Todas');
  buildChips('genChips', GENS, state.gens, 'Todos');
  document.querySelectorAll('#prodList input').forEach(cb=>cb.checked=true);
  updateProdSummary();
  renderAll();
});

function getFiltered(){
  return RAW.filter(r=>
    r.fecha >= state.from && r.fecha <= state.to &&
    state.cats.has(r.categoria) &&
    state.gens.has(r.genero) &&
    state.prods.has(r.producto)
  );
}

function sum(arr, fn){ return arr.reduce((a,r)=>a+fn(r),0); }
function groupSum(arr, keyFn){
  const m = new Map();
  arr.forEach(r=>{
    const k = keyFn(r);
    m.set(k, (m.get(k)||0) + r.total);
  });
  return m;
}

// ---- Chart.js setup ----
Chart.defaults.font.family = "'IBM Plex Sans', sans-serif";
Chart.defaults.color = '#6E5D4E';
Chart.defaults.borderColor = '#E6DDCC';

const PALETTE = {
  brown:'#6F4E37', brownLight:'#B99A7D', teal:'#2F6B5E', tealLight:'#8FBBAF', caramel:'#C17F3E', ink:'#2A1B12'
};

function baseOpts(extra){
  return Object.assign({
    responsive:true, maintainAspectRatio:false,
    plugins:{ legend:{display:false}, tooltip:{callbacks:{label:(ctx)=> ' ' + money(ctx.parsed.y ?? ctx.parsed.x ?? ctx.parsed)}} },
    scales:{
      x:{ grid:{display:false} },
      y:{ grid:{color:'#EFE8DA'}, ticks:{ callback:(v)=> '$'+v } }
    }
  }, extra||{});
}

let chartDaily, chartProduct, chartChannel, chartShift, chartGenderCat, chartNewReturning;

function initCharts(){
  chartDaily = new Chart(document.getElementById('chartDaily'), {
    type:'line',
    data:{ labels:[], datasets:[{ data:[], borderColor:PALETTE.brown, backgroundColor:'rgba(111,78,55,0.12)', fill:true, tension:0.25, pointRadius:3, pointBackgroundColor:PALETTE.brown }] },
    options: baseOpts({ plugins:{legend:{display:false}, tooltip:{callbacks:{label:(ctx)=>' '+money(ctx.parsed.y)}}} })
  });

  chartProduct = new Chart(document.getElementById('chartProduct'), {
    type:'bar',
    data:{ labels:[], datasets:[{ data:[], backgroundColor:PALETTE.brown, borderRadius:4 }] },
    options: Object.assign(baseOpts(), { indexAxis:'y', scales:{ x:{ grid:{color:'#EFE8DA'}, ticks:{callback:(v)=>'$'+v} }, y:{ grid:{display:false} } } })
  });

  chartChannel = new Chart(document.getElementById('chartChannel'), {
    type:'bar',
    data:{ labels:[], datasets:[{ data:[], backgroundColor:PALETTE.teal, borderRadius:4 }] },
    options: baseOpts()
  });

  chartShift = new Chart(document.getElementById('chartShift'), {
    type:'bar',
    data:{ labels:[], datasets:[{ data:[], backgroundColor:PALETTE.caramel, borderRadius:4 }] },
    options: baseOpts()
  });

  chartGenderCat = new Chart(document.getElementById('chartGenderCat'), {
    type:'bar',
    data:{ labels:[], datasets:[
      { label:'Hombre', data:[], backgroundColor:PALETTE.brown, borderRadius:4 },
      { label:'Mujer', data:[], backgroundColor:PALETTE.tealLight, borderRadius:4 }
    ]},
    options: Object.assign(baseOpts(), { plugins:{ legend:{display:true, position:'top', labels:{boxWidth:12}}, tooltip:{callbacks:{label:(ctx)=> ' '+ctx.dataset.label+': '+money(ctx.parsed.y)}} } })
  });

  chartNewReturning = new Chart(document.getElementById('chartNewReturning'), {
    type:'bar',
    data:{ labels:['Cliente nuevo','Cliente recurrente'], datasets:[
      { label:'Ingresos', data:[], backgroundColor:[PALETTE.caramel, PALETTE.teal], borderRadius:4, yAxisID:'y' }
    ]},
    options: Object.assign(baseOpts(), {
      indexAxis:'y',
      plugins:{ legend:{display:false}, tooltip:{callbacks:{label:(ctx)=> ' Ingresos: '+money(ctx.parsed.x) + '  ·  Pedidos: ' + ctx.raw_pedidos } } },
      scales:{ x:{ grid:{color:'#EFE8DA'}, ticks:{callback:(v)=>'$'+v} }, y:{ grid:{display:false} } }
    })
  });
}
initCharts();

function renderAll(){
  const data = getFiltered();

  // KPIs
  const ventasTotales = sum(data, r=>r.total);
  const pedidos = data.length;
  const ticketProm = pedidos ? ventasTotales/pedidos : 0;
  const clientesUnicos = new Set(data.map(r=>r.cliente_id)).size;
  const unidades = sum(data, r=>r.cantidad);

  document.getElementById('kpiVentas').textContent = money(ventasTotales);
  document.getElementById('kpiVentasSub').textContent = 'margen: no disponible en los datos';
  document.getElementById('kpiPedidos').textContent = pedidos;
  document.getElementById('kpiTicket').textContent = pedidos ? money(ticketProm) : '—';
  document.getElementById('kpiClientes').textContent = clientesUnicos;
  document.getElementById('kpiClientesSub').textContent = clientesUnicos ? Math.round((data.filter(r=>r.cliente_nuevo==='Sí').length/pedidos)*100) + '% pedidos de clientes nuevos' : '';
  document.getElementById('kpiUnidades').textContent = unidades;

  // Chart: daily
  const allDates = [];
  {
    let d = new Date(state.from+'T00:00:00');
    const end = new Date(state.to+'T00:00:00');
    while(d<=end){ allDates.push(d.toISOString().slice(0,10)); d.setDate(d.getDate()+1); }
  }
  const dailyMap = groupSum(data, r=>r.fecha);
  chartDaily.data.labels = allDates.map(d=> d.slice(8,10)+'/'+d.slice(5,7));
  chartDaily.data.datasets[0].data = allDates.map(d=> dailyMap.get(d)||0);
  chartDaily.update();

  // Chart: product
  const prodMap = groupSum(data, r=>r.producto);
  const prodSorted = [...prodMap.entries()].sort((a,b)=>b[1]-a[1]);
  chartProduct.data.labels = prodSorted.map(e=>e[0]);
  chartProduct.data.datasets[0].data = prodSorted.map(e=>e[1]);
  chartProduct.update();

  // Chart: channel
  const chMap = groupSum(data, r=>r.canal);
  const chSorted = [...chMap.entries()].sort((a,b)=>b[1]-a[1]);
  chartChannel.data.labels = chSorted.map(e=>e[0]);
  chartChannel.data.datasets[0].data = chSorted.map(e=>e[1]);
  chartChannel.update();

  // Chart: shift
  const shMap = groupSum(data, r=>r.turno);
  chartShift.data.labels = SHIFT_ORDER.filter(s=>shMap.has(s));
  chartShift.data.datasets[0].data = chartShift.data.labels.map(s=>shMap.get(s)||0);
  chartShift.update();

  // Chart: gender x category
  const gcLabels = CATS;
  const menData = gcLabels.map(c=> sum(data.filter(r=>r.categoria===c && r.genero==='Hombre'), r=>r.total));
  const womenData = gcLabels.map(c=> sum(data.filter(r=>r.categoria===c && r.genero==='Mujer'), r=>r.total));
  chartGenderCat.data.labels = gcLabels;
  chartGenderCat.data.datasets[0].data = menData;
  chartGenderCat.data.datasets[1].data = womenData;
  chartGenderCat.update();

  // Chart: new vs returning
  const nuevos = data.filter(r=>r.cliente_nuevo==='Sí');
  const recurrentes = data.filter(r=>r.cliente_nuevo==='No');
  chartNewReturning.data.datasets[0].data = [sum(nuevos,r=>r.total), sum(recurrentes,r=>r.total)];
  chartNewReturning.options.plugins.tooltip.callbacks.label = (ctx)=>{
    const pedidosN = ctx.dataIndex===0 ? nuevos.length : recurrentes.length;
    return ' Ingresos: ' + money(ctx.parsed.x) + '  ·  Pedidos: ' + pedidosN;
  };
  chartNewReturning.update();

  renderHeatmap(data);
  renderClients(data);
}

function renderHeatmap(data){
  const wrap = document.getElementById('heatmapWrap');
  const emptyMsg = document.getElementById('heatmapEmpty');
  if(data.length===0){ wrap.innerHTML=''; emptyMsg.style.display='block'; return; }
  emptyMsg.style.display='none';

  const prodsPresent = [...new Set(data.map(r=>r.producto))].sort();
  const daysPresent = DAY_ORDER.filter(d=> data.some(r=>r.dia_semana===d));
  const matrix = {};
  let max = 0;
  prodsPresent.forEach(p=>{
    matrix[p] = {};
    daysPresent.forEach(d=>{
      const v = sum(data.filter(r=>r.producto===p && r.dia_semana===d), r=>r.total);
      matrix[p][d] = v;
      if(v>max) max = v;
    });
  });

  let html = '<table class="data-table"><thead><tr><th class="prod-name">Producto</th>';
  daysPresent.forEach(d=> html += '<th>'+DAY_ES[d]+'</th>');
  html += '</tr></thead><tbody>';
  prodsPresent.forEach(p=>{
    html += '<tr><td class="prod-name">'+p+'</td>';
    daysPresent.forEach(d=>{
      const v = matrix[p][d];
      const alpha = max? (v/max) : 0;
      const bg = v===0 ? 'transparent' : 'rgba(111,78,55,'+(0.12+alpha*0.72).toFixed(2)+')';
      const color = alpha>0.55 ? '#fff' : 'var(--ink)';
      html += '<td style="background:'+bg+'; color:'+color+';">'+(v? '$'+v : '–')+'</td>';
    });
    html += '</tr>';
  });
  html += '</tbody></table>';
  wrap.innerHTML = html;
}

function renderClients(data){
  const tbody = document.querySelector('#clientsTable tbody');
  const emptyMsg = document.getElementById('clientsEmpty');
  const byClient = new Map();
  data.forEach(r=>{
    if(!byClient.has(r.cliente_id)) byClient.set(r.cliente_id, []);
    byClient.get(r.cliente_id).push(r);
  });
  const recurrentRows = [...byClient.entries()]
    .filter(([id, rows])=> rows.length>=2)
    .map(([id, rows])=>{
      const ingreso = sum(rows, r=>r.total);
      const zonaCounts = {};
      rows.forEach(r=> zonaCounts[r.zona] = (zonaCounts[r.zona]||0)+1);
      const zonaTop = Object.entries(zonaCounts).sort((a,b)=>b[1]-a[1])[0][0];
      return { id, compras: rows.length, ingreso, ticket: ingreso/rows.length, zona: zonaTop };
    })
    .sort((a,b)=>b.ingreso-a.ingreso);

  if(recurrentRows.length===0){
    tbody.innerHTML=''; emptyMsg.style.display='block';
  } else {
    emptyMsg.style.display='none';
    tbody.innerHTML = recurrentRows.map(r=>
      '<tr><td>'+r.id+'</td><td>'+r.compras+'</td><td>'+money(r.ingreso)+'</td><td>'+money(r.ticket)+'</td><td>'+r.zona+'</td></tr>'
    ).join('');
  }
}

updateProdSummary();
renderAll();
</script>
</body>
</html>
