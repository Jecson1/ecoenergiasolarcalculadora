<!DOCTYPE html>
<html lang="pt-BR">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculadora de Economia - Energia Solar | ECO ENERGIA SOLAR</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #1e3c72, #2a5298, #4CAF50);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .calculator-container {
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
      max-width: 600px;
      width: 100%;
      padding: 40px;
      animation: slideUp 0.8s ease-out;
    }

    @keyframes slideUp {
      from {
        opacity: 0;
        transform: translateY(50px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .header {
      text-align: center;
      margin-bottom: 30px;
    }

    .logo {
      font-size: 2.5em;
      font-weight: bold;
      background: linear-gradient(45deg, #4CAF50, #2196F3);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 10px;
    }

    .subtitle {
      color: #666;
      font-size: 1.1em;
      margin-bottom: 20px;
    }

    .form-group {
      margin-bottom: 25px;
    }

    label {
      display: block;
      font-weight: 600;
      color: #333;
      margin-bottom: 8px;
      font-size: 1.1em;
    }

    input[type="number"],
    select {
      width: 100%;
      padding: 15px;
      border: 2px solid #e0e0e0;
      border-radius: 10px;
      font-size: 1.1em;
      transition: all 0.3s ease;
      background: #f9f9f9;
    }

    input[type="number"]:focus,
    select:focus {
      outline: none;
      border-color: #4CAF50;
      background: white;
      box-shadow: 0 0 10px rgba(76, 175, 80, 0.2);
    }

    .calculate-btn {
      width: 100%;
      padding: 18px;
      background: linear-gradient(45deg, #4CAF50, #45a049);
      color: white;
      border: none;
      border-radius: 12px;
      font-size: 1.2em;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.3s ease;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .calculate-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 20px rgba(76, 175, 80, 0.3);
    }

    .results {
      margin-top: 30px;
      padding: 25px;
      background: linear-gradient(135deg, #f8f9fa, #e9ecef);
      border-radius: 15px;
      border-left: 5px solid #4CAF50;
      display: none;
    }

    .result-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 15px;
      padding: 10px 0;
      border-bottom: 1px solid #ddd;
    }

    .result-item:last-child {
      border-bottom: none;
      font-size: 1.3em;
      font-weight: bold;
      color: #4CAF50;
    }

    .result-label {
      font-weight: 600;
      color: #333;
    }

    .result-value {
      font-weight: bold;
      color: #2196F3;
    }

    .savings-highlight {
      background: linear-gradient(45deg, #4CAF50, #66BB6A);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      font-size: 1.5em !important;
    }

    .contact-section {
      margin-top: 30px;
      text-align: center;
      padding: 20px;
      background: linear-gradient(45deg, #4CAF50, #2196F3);
      border-radius: 15px;
      color: white;
    }

    .contact-section h3 {
      margin-bottom: 10px;
      font-size: 1.3em;
    }

    .contact-section p {
      font-size: 1.1em;
      opacity: 0.9;
    }

    .sun-icon {
      font-size: 3em;
      color: #FFC107;
      margin-bottom: 10px;
      animation: rotate 20s linear infinite;
    }

    @media (max-width: 768px) {
      .calculator-container {
        padding: 25px;
        margin: 10px;
      }

      .logo {
        font-size: 2em;
      }
    }
  </style>
</head>

<body>
  <div class="calculator-container">
    <div class="header">
      <div class="sun-icon" ☀️</div>
        <div class="logo">ECO ENERGIA SOLAR</div>
        <div class="subtitle">Descubra quanto você pode economizar com energia solar</div>
      </div>

      <form id="solarCalculator">
        <div class="form-group">
          <label for="monthlyBill">💰 Valor da sua conta de luz mensal (R$):</label>
          <input type="number" id="monthlyBill" min="50" max="5000" step="0.01" required placeholder="Ex: 350,00">
        </div>

        <div class="form-group">
          <label for="consumption">⚡ Consumo mensal em kWh (opcional):</label>
          <input type="number" id="consumption" min="0" max="2000" step="1" placeholder="Ex: 450 kWh">
        </div>

        <div class="form-group">
          <label for="roofType">🏠 Tipo do seu telhado:</label>
          <select id="roofType" required>
            <option value="">Selecione o tipo</option>
            <option value="ceramico">Cerâmico/Colonial</option>
            <option value="metalico">Metálico/Galvanizado</option>
            <option value="fibrocimento">Fibrocimento</option>
            <option value="laje">Laje</option>
          </select>
        </div>

        <div class="form-group">
          <label for="region">📍 Região:</label>
          <select id="region" required>
            <option value="">Selecione sua região</option>
            <option value="amapa">Amapá</option>
            <option value="norte">Norte (outros estados)</option>
            <option value="nordeste">Nordeste</option>
            <option value="centro-oeste">Centro-Oeste</option>
            <option value="sudeste">Sudeste</option>
            <option value="sul">Sul</option>
          </select>
        </div>

        <button type="submit" class="calculate-btn">🔆 Calcular Economia</button>
      </form>

      <div id="results" class="results">
        <h3 style="color: #4CAF50; margin-bottom: 20px; text-align: center;">💚 Seus Resultados</h3>
        <div class="result-item">
          <span class="result-label">Consumo estimado:</span>
          <span class="result-value" id="estimatedConsumption">-</span>
        </div>
        <div class="result-item">
          <span class="result-label">Potência necessária:</span>
          <span class="result-value" id="systemPower">-</span>
        </div>
        <div class="result-item">
          <span class="result-label">Economia mensal:</span>
          <span class="result-value" id="monthlySavings">-</span>
        </div>
        <div class="result-item">
          <span class="result-label">Economia anual:</span>
          <span class="result-value" id="yearlySavings">-</span>
        </div>
        <div class="result-item">
          <span class="result-label">Economia em 25 anos:</span>
          <span class="result-value savings-highlight" id="totalSavings">-</span>
        </div>
      </div>

      <div class="contact-section">
        <h3>🌟 Pronto para começar a economizar?</h3>
        <p>Entre em contato conosco para um orçamento personalizado!</p>
        <p><strong>ECO ENERGIA SOLAR - Energia limpa para o Amapá</strong></p>
      </div>
    </div>

    <script>
      document.getElementById('solarCalculator').addEventListener('submit', function(e) {
        e.preventDefault();
        const monthlyBill = parseFloat(document.getElementById('monthlyBill').value);
        const consumption = parseFloat(document.getElementById('consumption').value) || 0;
        const roofType = document.getElementById('roofType').value;
        const region = document.getElementById('region').value;
        // Tarifas médias por região (R$/kWh)
        const tariffs = {
          'amapa': 0.65,
          'norte': 0.60,
          'nordeste': 0.58,
          'centro-oeste': 0.62,
          'sudeste': 0.68,
          'sul': 0.70
        };
        const tariff = tariffs[region] || 0.65;
        // Calcular consumo se não foi informado
        let estimatedConsumption = consumption;
        if (consumption === 0) {
          estimatedConsumption = Math.round((monthlyBill / tariff) * 0.85); // 85% para descontar taxa mínima
        }
        // Irradiação solar média por região (kWh/m²/dia)
        const solarIrradiation = {
          'amapa': 5.2,
          'norte': 5.0,
          'nordeste': 5.8,
          'centro-oeste': 5.5,
          'sudeste': 4.8,
          'sul': 4.2
        };
        const irradiation = solarIrradiation[region] || 5.2;
        // Calcular potência necessária (kWp)
        const systemPower = Math.round((estimatedConsumption / (irradiation * 30 * 0.8)) * 100) / 100;
        // Calcular economias
        const monthlySavings = monthlyBill * 0.85; // 85% de economia média
        const yearlySavings = monthlySavings * 12;
        const totalSavings = yearlySavings * 25; // Vida útil de 25 anos
        // Mostrar resultados
        document.getElementById('estimatedConsumption').textContent = estimatedConsumption + ' kWh/mês';
        document.getElementById('systemPower').textContent = systemPower + ' kWp';
        document.getElementById('monthlySavings').textContent = 'R$ ' + monthlySavings.toFixed(2).replace('.', ',');
        document.getElementById('yearlySavings').textContent = 'R$ ' + yearlySavings.toFixed(2).replace('.', ',');
        document.getElementById('totalSavings').textContent = 'R$ ' + totalSavings.toLocaleString('pt-BR', {
          minimumFractionDigits: 2
        });
        // Mostrar seção de resultados com animação
        const resultsDiv = document.getElementById('results');
        resultsDiv.style.display = 'block';
        resultsDiv.scrollIntoView({
          behavior: 'smooth',
          block: 'nearest'
        });
      });
      // Formatação automática do valor monetário
      document.getElementById('monthlyBill').addEventListener('input', function(e) {
        let value = e.target.value;
        if (value) {
          e.target.value = value;
        }
      });
    </script>
</body>

</html>
