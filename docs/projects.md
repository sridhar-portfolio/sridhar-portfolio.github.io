<style>
  a p {
    position: relative;
    display: inline-block;
  }

  a p::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 2px;
    background-color: #007acc;
    bottom: 0;
    left: 0;
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }

  a:hover p::after {
    transform: scaleX(1);
  }
  </style>


<div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center;">

  <div style="flex: 0 0 calc(50% - 20px); box-sizing: border-box; border: 1px solid #ccc; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
    <a href="rfm_1.html" style="text-decoration: none; color: inherit;">
      <img src="../assets/img/rfm_1_01.jpg" alt="RFM Analysis" style="width: 100%; height: 150px; object-fit: cover;">
      <p style="padding: 10px; text-align: center;">Wie man mithilfe der RFM-Analyse im Onlinehandel High-Value-Kunden identifiziert</p>
    </a>
  </div>

  <div style="flex: 0 0 calc(50% - 20px); box-sizing: border-box; border: 1px solid #ccc; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
    <a href="pareto_1.html" style="text-decoration: none; color: inherit;">
      <img src="../assets/img/pareto_1_0.jpg" alt="Pareto Analysis" style="width: 100%; height: 150px; object-fit: cover;">
      <p style="padding: 10px; text-align: center;">Pareto trifft E-Commerce: Entlarvt die Datenanalyse den 80/20-Mythos?</p>
    </a>
  </div>

  <!-- Repeat for other projects -->

</div>
