# Etiqueta-de-Envio-
Preencha e envie cartas pacotes e adeus dificuldades 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Etiqueta de Envio Profesional</title>
  <style>
    :root {
      --primary: #0a5fc2;
      --primary-dark: #0c4e9d;
      --secondary: #eaf3ff;
      --bg: #f4f7fb;
      --card: #ffffff;
      --text: #1d1d1d;
      --muted: #5f6874;
      --line: #dfe6f0;
      --danger: #d93025;
      --success: #188038;
      --shadow: 0 6px 18px rgba(0, 0, 0, 0.08);
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: "Segoe UI", Arial, sans-serif;
      background: var(--bg);
      color: var(--text);
    }

    .container {
      max-width: 1100px;
      margin: 30px auto;
      background: var(--card);
      border-radius: 18px;
      box-shadow: var(--shadow);
      padding: 24px;
      border: 1px solid var(--line);
    }

    h2 {
      margin: 0 0 20px;
      font-size: 2rem;
      color: var(--primary-dark);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(240px, 1fr));
      gap: 16px;
    }

    .field {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .field.full {
      grid-column: 1 / -1;
    }

    label {
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--text);
    }

    input, select {
      width: 100%;
      padding: 11px 12px;
      border: 1px solid var(--line);
      border-radius: 10px;
      font-size: 1rem;
      background: #fff;
      transition: 0.2s ease;
    }

    input:focus, select:focus {
      outline: none;
      border-color: var(--primary);
      box-shadow: 0 0 0 3px rgba(10, 95, 194, 0.14);
    }

    .actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 20px;
      margin-bottom: 12px;
    }

    .btn {
      appearance: none;
      border: none;
      border-radius: 10px;
      padding: 12px 18px;
      font-weight: 700;
      cursor: pointer;
      transition: 0.2s ease;
    }

    .btn:hover {
      transform: translateY(-1px);
    }

    .btn-primary {
      background: var(--primary);
      color: white;
    }

    .btn-primary:hover {
      background: var(--primary-dark);
    }

    .btn-secondary {
      background: var(--secondary);
      color: var(--primary-dark);
    }

    .status {
      min-height: 24px;
      margin-top: 6px;
      font-size: 0.95rem;
      color: var(--muted);
    }

    .status.error {
      color: var(--danger);
      font-weight: 600;
    }

    .status.success {
      color: var(--success);
      font-weight: 600;
    }

    .preview-wrap {
      margin-top: 28px;
      border-top: 1px solid var(--line);
      padding-top: 22px;
    }

    .preview-title {
      margin-bottom: 14px;
      font-size: 1.1rem;
      font-weight: 700;
      color: var(--primary-dark);
    }

    .label-preview {
      width: 100%;
      max-width: 900px;
      min-height: 520px;
      border: 2px solid var(--line);
      border-radius: 18px;
      background: #fff;
      padding: 18px;
      box-shadow: inset 0 0 0 1px rgba(0,0,0,0.02);
    }

    .label-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 2px solid #eceff4;
      padding-bottom: 12px;
      margin-bottom: 16px;
    }

    .label-header h3 {
      margin: 0;
      font-size: 1.7rem;
      color: var(--primary-dark);
    }

    .badge {
      background: var(--secondary);
      color: var(--primary-dark);
      padding: 8px 12px;
      border-radius: 999px;
      font-weight: 700;
      font-size: 0.85rem;
    }

    .label-body {
      display: grid;
      grid-template-columns: 1.7fr 1fr;
      gap: 18px;
    }

    .box {
      border: 1px solid var(--line);
      border-radius: 12px;
      padding: 14px;
      background: #fcfdff;
    }

    .box h4 {
      margin: 0 0 12px;
      font-size: 1rem;
      color: var(--primary-dark);
      text-transform: uppercase;
      letter-spacing: 0.04em;
    }

    .info-line {
      margin-bottom: 8px;
      line-height: 1.5;
      font-size: 0.97rem;
    }

    .qr-box {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 10px;
      min-height: 240px;
    }

    .barcode-wrap, .cep-wrap {
      margin-top: 14px;
      text-align: center;
    }

    .barcode-wrap canvas, .cep-wrap canvas, .qr-box canvas {
      width: 100%;
      max-width: 220px;
      height: auto;
      display: block;
      margin: 0 auto;
      border: 1px solid var(--line);
      border-radius: 8px;
      background: white;
      padding: 8px;
    }

    @media (max-width: 800px) {
      .grid, .label-body {
        grid-template-columns: 1fr;
      }
    }

    @media print {
      body {
        background: white;
      }

      .container {
        box-shadow: none;
        border: none;
        margin: 0;
        padding: 0;
      }

      .controls, .actions, .status, .preview-wrap .preview-title {
        display: none !important;
      }

      .label-preview {
        max-width: none;
        width: 100%;
        min-height: auto;
        border: none;
        padding: 0;
        box-shadow: none;
      }

      .label-header, .label-body, .box {
        break-inside: avoid;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="controls">
      <h2>Etiqueta de Envio</h2>

      <div class="grid">
        <div class="field full">
          <label for="remetenteNome">Nome do remetente:</label>
          <input id="remetenteNome" type="text" placeholder="Ex.: Loja Central Ltda.">
        </div>

        <div class="field">
          <label for="remetenteCpfCnpj">CPF/CNPJ do remetente:</label>
          <input id="remetenteCpfCnpj" type="text" placeholder="000.000.000-00 ou 00.000.000/0000-00">
        </div>

        <div class="field">
          <label for="remetenteTelefone">Telefone:</label>
          <input id="remetenteTelefone" type="text" placeholder="(11) 99999-9999">
        </div>

        <div class="field full">
          <label for="destNome">Nome do destinatário:</label>
          <input id="destNome" type="text" placeholder="Ex.: João da Silva">
        </div>

        <div class="field">
          <label for="destCep">CEP do destinatário:</label>
          <input id="destCep" type="text" maxlength="9" placeholder="00000-000">
        </div>

        <div class="field">
          <label for="destRastreio">Código de rastreio:</label>
          <input id="destRastreio" type="text" placeholder="Ex.: BR123456789BR">
        </div>

        <div class="field">
          <label for="destRua">Rua:</label>
          <input id="destRua" type="text" placeholder="Rua das Flores">
        </div>

        <div class="field">
          <label for="destNumero">Número:</label>
          <input id="destNumero" type="text" placeholder="123">
        </div>

        <div class="field">
          <label for="destCidade">Cidade:</label>
          <input id="destCidade" type="text" placeholder="São Paulo">
        </div>

        <div class="field">
          <label for="destEstado">Estado:</label>
          <input id="destEstado" type="text" placeholder="SP">
        </div>

        <div class="field">
          <label for="peso">Peso (kg):</label>
          <input id="peso" type="number" min="0.1" step="0.1" placeholder="1.5">
        </div>

        <div class="field">
          <label for="embalagem">Tipo de embalagem:</label>
          <select id="embalagem">
            <option value="Caixa">Caixa</option>
            <option value="Envelope">Envelope</option>
            <option value="Pacote">Pacote</option>
            <option value="Pallet">Pallet</option>
          </select>
        </div>

        <div class="field">
          <label for="servico">Serviço:</label>
          <select id="servico">
            <option value="PAC">Correios - PAC</option>
            <option value="SEDEX">Correios - SEDEX</option>
            <option value="FEDEX">FedEx</option>
            <option value="JADLOG">Jadlog</option>
            <option value="EXPRESSO">Expresso</option>
          </select>
        </div>

        <div class="field">
          <label for="tipoEntrega">Tipo de entrega:</label>
          <select id="tipoEntrega">
            <option value="Normal">Normal</option>
            <option value="Expressa">Expressa</option>
            <option value="Agendada">Agendada</option>
            <option value="Internacional">Internacional</option>
          </select>
        </div>
      </div>

      <div class="actions">
        <button class="btn btn-primary" onclick="gerarEtiqueta()">Gerar PDF</button>
        <button class="btn btn-secondary" onclick="imprimirEtiqueta()">Imprimir</button>
        <button class="btn btn-secondary" onclick="voz()">Preencher por voz</button>
      </div>

      <div id="status" class="status" aria-live="polite"></div>
    </div>

    <div class="preview-wrap">
      <div class="preview-title">Pré-visualização da etiqueta</div>

      <div class="label-preview" id="labelPreview">
        <div class="label-header">
          <h3>Etiqueta de Envio</h3>
          <span class="badge" id="badgeServico">PAC</span>
        </div>

        <div class="label-body">
          <div>
            <div class="box">
              <h4>Remetente</h4>
              <div class="info-line" id="previewRemetenteNome">-</div>
              <div class="info-line" id="previewRemetenteDocs">-</div>
              <div class="info-line" id="previewRemetenteTel">-</div>
            </div>

            <div class="box" style="margin-top: 14px;">
              <h4>Destinatário</h4>
              <div class="info-line" id="previewDestNome">-</div>
              <div class="info-line" id="previewDestEndereco">-</div>
              <div class="info-line" id="previewDestCidade">-</div>
              <div class="info-line" id="previewDestCep">-</div>
            </div>
          </div>

          <div class="qr-box">
            <canvas id="qrcode"></canvas>
            <div class="info-line" id="previewRastreio">Rastreio: -</div>
            <div class="info-line" id="previewPeso">Peso: -</div>
            <div class="info-line" id="previewEmbalagem">Embalagem: -</div>
          </div>
        </div>

        <div class="barcode-wrap">
          <canvas id="barcode"></canvas>
        </div>

        <div class="cep-wrap">
          <canvas id="cepbarcode"></canvas>
        </div>
      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/jsbarcode@3.11.6/dist/JsBarcode.all.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/qrcode/build/qrcode.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>

  <script>
    const statusEl = document.getElementById("status");

    function setStatus(message, type = "") {
      statusEl.textContent = message;
      statusEl.className = "status";
      if (type) statusEl.classList.add(type);
    }

    function formatCEP(value) {
      const onlyDigits = value.replace(/\D/g, "").slice(0, 8);
      if (onlyDigits.length <= 5) return onlyDigits;
      return `${onlyDigits.slice(0, 5)}-${onlyDigits.slice(5)}`;
    }

    function formatTelefone(value) {
      const digits = value.replace(/\D/g, "").slice(0, 11);
      if (digits.length <= 2) return digits;
      if (digits.length <= 7) return `(${digits.slice(0, 2)}) ${digits.slice(2)}`;
      if (digits.length <= 11) {
        return `(${digits.slice(0, 2)}) ${digits.slice(2, 7)}-${digits.slice(7)}`;
      }
      return `(${digits.slice(0, 2)}) ${digits.slice(2, 7)}-${digits.slice(7, 11)}`;
    }

    function formatCpfCnpj(value) {
      const digits = value.replace(/\D/g, "").slice(0, 14);

      if (digits.length <= 11) {
        if (digits.length <= 3) return digits;
        if (digits.length <= 6) return `${digits.slice(0, 3)}.${digits.slice(3)}`;
        return `${digits.slice(0, 3)}.${digits.slice(3, 6)}.${digits.slice(6)}`;
      }

      if (digits.length <= 12) {
        return `${digits.slice(0, 2)}.${digits.slice(2, 5)}.${digits.slice(5, 8)}/${digits.slice(8)}`;
      }

      return `${digits.slice(0, 2)}.${digits.slice(2, 5)}.${digits.slice(5, 8)}/${digits.slice(8, 12)}-${digits.slice(12)}`;
    }

    document.getElementById("destCep").addEventListener("input", (e) => {
      e.target.value = formatCEP(e.target.value);
    });

    document.getElementById("remetenteTelefone").addEventListener("input", (e) => {
      e.target.value = formatTelefone(e.target.value);
    });

    document.getElementById("remetenteCpfCnpj").addEventListener("input", (e) => {
      e.target.value = formatCpfCnpj(e.target.value);
    });

    async function buscarCEP() {
      const input = document.getElementById("destCep");
      const cep = input.value.replace(/\D/g, "");

      if (cep.length !== 8) {
        setStatus("Informe um CEP válido com 8 dígitos.", "error");
        return;
      }

      try {
        setStatus("Buscando endereço pelo CEP...");
        const response = await fetch(`https://viacep.com.br/ws/${cep}/json/`);
        const data = await response.json();

        if (data.erro) {
          setStatus("CEP não encontrado.", "error");
          return;
        }

        document.getElementById("destRua").value = data.logradouro || "";
        document.getElementById("destCidade").value = data.localidade || "";
        document.getElementById("destEstado").value = data.uf || "";

        setStatus("Endereço preenchido automaticamente.", "success");
      } catch (error) {
        console.error(error);
        setStatus("Não foi possível consultar o CEP. Verifique sua conexão.", "error");
      }
    }

    document.getElementById("destCep").addEventListener("blur", buscarCEP);

    function validarCPFouCNPJ(value) {
      const digits = value.replace(/\D/g, "");
      if (!digits) return false;

      if (digits.length === 11) {
        return digits.length === 11;
      }

      if (digits.length === 14) {
        return digits.length === 14;
      }

      return false;
    }

    function validarFormulario() {
      const remetenteNome = document.getElementById("remetenteNome").value.trim();
      const remetenteCpfCnpj = document.getElementById("remetenteCpfCnpj").value.trim();
      const destNome = document.getElementById("destNome").value.trim();
      const destCep = document.getElementById("destCep").value.trim();
      const destRua = document.getElementById("destRua").value.trim();
      const destNumero = document.getElementById("destNumero").value.trim();
      const destCidade = document.getElementById("destCidade").value.trim();
      const destEstado = document.getElementById("destEstado").value.trim();
      const rastreio = document.getElementById("destRastreio").value.trim();
      const peso = document.getElementById("peso").value.trim();
      const servico = document.getElementById("servico").value;

      if (!remetenteNome || !remetenteCpfCnpj || !destNome || !destCep || !destRua || !destNumero || !destCidade || !destEstado || !rastreio || !peso || !servico) {
        setStatus("Preencha todos os campos obrigatórios antes de gerar a etiqueta.", "error");
        return false;
      }

      if (!validarCPFouCNPJ(remetenteCpfCnpj)) {
        setStatus("CPF/CNPJ do remetente inválido.", "error");
        return false;
      }

      if (destCep.replace(/\D/g, "").length !== 8) {
        setStatus("CEP do destinatário inválido.", "error");
        return false;
      }

      if (Number(peso) <= 0) {
        setStatus("Informe um peso válido em quilogramas.", "error");
        return false;
      }

      return true;
    }

    function atualizarPreview() {
      const remetenteNome = document.getElementById("remetenteNome").value || "-";
      const remetenteCpfCnpj = document.getElementById("remetenteCpfCnpj").value || "-";
      const remetenteTelefone = document.getElementById("remetenteTelefone").value || "-";
      const destNome = document.getElementById("destNome").value || "-";
      const destRua = document.getElementById("destRua").value || "-";
      const destNumero = document.getElementById("destNumero").value || "-";
      const destCidade = document.getElementById("destCidade").value || "-";
      const destEstado = document.getElementById("destEstado").value || "-";
      const destCep = document.getElementById("destCep").value || "-";
      const rastreio = document.getElementById("destRastreio").value || "-";
      const peso = document.getElementById("peso").value || "-";
      const embalagem = document.getElementById("embalagem").value || "-";
      const servico = document.getElementById("servico").value || "PAC";

      document.getElementById("badgeServico").textContent = servico;
      document.getElementById("previewRemetenteNome").textContent = remetenteNome;
      document.getElementById("previewRemetenteDocs").textContent = `CPF/CNPJ: ${remetenteCpfCnpj}`;
      document.getElementById("previewRemetenteTel").textContent = `Telefone: ${remetenteTelefone}`;
      document.getElementById("previewDestNome").textContent = destNome;
      document.getElementById("previewDestEndereco").textContent = `End.: ${destRua}, ${destNumero}`;
      document.getElementById("previewDestCidade").textContent = `${destCidade} - ${destEstado}`;
      document.getElementById("previewDestCep").textContent = `CEP: ${destCep}`;
      document.getElementById("previewRastreio").textContent = `Rastreio: ${rastreio}`;
      document.getElementById("previewPeso").textContent = `Peso: ${peso} kg`;
      document.getElementById("previewEmbalagem").textContent = `Embalagem: ${embalagem}`;
    }

    function gerarBarras() {
      const rastreio = document.getElementById("destRastreio").value.trim();
      const cep = document.getElementById("destCep").value.trim();

      if (!rastreio) return;

      try {
        JsBarcode("#barcode", rastreio, {
          format: "CODE128",
          displayValue: true,
          fontSize: 11,
          width: 2,
          height: 60,
          margin: 12
        });
      } catch (e) {
        console.error("Erro no código de barras do rastreio:", e);
      }

      if (cep) {
        try {
          JsBarcode("#cepbarcode", cep.replace(/\D/g, ""), {
            format: "CODE128",
            displayValue: true,
            fontSize: 11,
            width: 2,
            height: 60,
            margin: 12
          });
        } catch (e) {
          console.error("Erro no código de barras do CEP:", e);
        }
      }
    }

    function gerarQRCode(dados) {
      const canvas = document.getElementById("qrcode");

      if (!canvas) return;

      try {
        QRCode.toCanvas(canvas, dados, {
          width: 180,
          margin: 1,
          color: {
            dark: "#000000",
            light: "#ffffff"
          }
        });
      } catch (e) {
        console.error("Erro ao gerar QR Code:", e);
      }
    }

    function voz() {
      const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;

      if (!SpeechRecognition) {
        setStatus("Seu navegador não suporta reconhecimento de voz.", "error");
        return;
      }

      const recognition = new SpeechRecognition();
      recognition.lang = "pt-BR";
      recognition.interimResults = false;
      recognition.maxAlternatives = 1;

      setStatus("Ouvindo... fale o nome do destinatário.");

      recognition.start();

      recognition.onresult = (event) => {
        const texto = event.results[0][0].transcript;
        document.getElementById("destNome").value = texto.trim();
        setStatus("Nome do destinatário preenchido por voz.", "success");
        atualizarPreview();
      };

      recognition.onerror = () => {
        setStatus("Não foi possível ouvir o nome. Tente novamente.", "error");
      };
    }

    function imprimirEtiqueta() {
      if (!validarFormulario()) return;

      atualizarPreview();
      gerarBarras();
      const dados = [
        `Remetente: ${document.getElementById("remetenteNome").value.trim()}`,
        `CPF/CNPJ: ${document.getElementById("remetenteCpfCnpj").value.trim()}`,
        `Destinatário: ${document.getElementById("destNome").value.trim()}`,
        `Endereço: ${document.getElementById("destRua").value.trim()}, ${document.getElementById("destNumero").value.trim()}`,
        `Cidade: ${document.getElementById("destCidade").value.trim()} - ${document.getElementById("destEstado").value.trim()}`,
        `CEP: ${document.getElementById("destCep").value.trim()}`,
        `Rastreio: ${document.getElementById("destRastreio").value.trim()}`,
        `Serviço: ${document.getElementById("servico").value}`,
        `Embalagem: ${document.getElementById("embalagem").value}`,
        `Peso: ${document.getElementById("peso").value} kg`
      ].join("\n");

      gerarQRCode(dados);
      setStatus("Etiqueta pronta para impressão.", "success");
      window.print();
    }

    function gerarEtiqueta() {
      if (!validarFormulario()) return;

      atualizarPreview();

      const nomeDest = document.getElementById("destNome").value.trim();
      const cep = document.getElementById("destCep").value.trim();
      const rua = document.getElementById("destRua").value.trim();
      const numero = document.getElementById("destNumero").value.trim();
      const cidade = document.getElementById("destCidade").value.trim();
      const estado = document.getElementById("destEstado").value.trim();
      const rastreio = document.getElementById("destRastreio").value.trim();
      const servico = document.getElementById("servico").value;
      const peso = document.getElementById("peso").value.trim();
      const embalagem = document.getElementById("embalagem").value;
      const remetenteNome = document.getElementById("remetenteNome").value.trim();
      const remetenteCpfCnpj = document.getElementById("remetenteCpfCnpj").value.trim();

      setStatus("Gerando PDF...", "success");

      gerarBarras();

      const dados = [
        `Remetente: ${remetenteNome}`,
        `CPF/CNPJ: ${remetenteCpfCnpj}`,
        `Destinatário: ${nomeDest}`,
        `CEP: ${cep}`,
        `Endereço: ${rua}, ${numero}`,
        `Cidade: ${cidade} - ${estado}`,
        `Rastreio: ${rastreio}`,
        `Serviço: ${servico}`,
        `Embalagem: ${embalagem}`,
        `Peso: ${peso} kg`
      ].join("\n");

      gerarQRCode(dados);

      try {
        const { jsPDF } = window.jspdf;
        const doc = new jsPDF({
          orientation: "portrait",
          unit: "mm",
          format: "a4"
        });

        const pageW = doc.internal.pageSize.getWidth();
        const pageH = doc.internal.pageSize.getHeight();

        doc.setFillColor(245, 247, 250);
        doc.rect(0, 0, pageW, pageH, "F");

        doc.setDrawColor(213, 222, 234);
        doc.setLineWidth(0.5);
        doc.rect(8, 8, pageW - 16, pageH - 16);

        doc.setTextColor(12, 79, 157);
        doc.setFont("helvetica", "bold");
        doc.setFontSize(24);
        doc.text("Etiqueta de Envio", 16, 22);

        doc.setTextColor(0, 0, 0);
        doc.setFont("helvetica", "normal");
        doc.setFontSize(12);

        doc.text(`Remetente: ${remetenteNome}`, 16, 35);
        doc.text(`CPF/CNPJ: ${remetenteCpfCnpj}`, 16, 42);
        doc.text(`Destinatário: ${nomeDest}`, 16, 52);
        doc.text(`Endereço: ${rua}, ${numero}`, 16, 60);
        doc.text(`Cidade: ${cidade} - ${estado}`, 16, 68);
        doc.text(`CEP: ${cep}`, 16, 76);
        doc.text(`Serviço: ${servico}`, 16, 84);
        doc.text(`Peso: ${peso} kg`, 16, 92);
        doc.text(`Embalagem: ${embalagem}`, 16, 100);
        doc.text(`Rastreio: ${rastreio}`, 16, 108);

        const qrData = document.getElementById("qrcode").toDataURL("image/png");
        doc.addImage(qrData, "PNG", 150, 26, 42, 42);

        const barcodeImg = document.getElementById("barcode").toDataURL("image/png");
        doc.addImage(barcodeImg, "PNG", 16, 122, 130, 24);

        const cepImg = document.getElementById("cepbarcode").toDataURL("image/png");
        doc.addImage(cepImg, "PNG", 16, 150, 130, 24);

        doc.setFont("helvetica", "bold");
        doc.text("Código de barras do rastreio", 16, 118);
        doc.text("Código de barras do CEP", 16, 146);

        doc.save("etiqueta-envio.pdf");
        setStatus("PDF gerado com sucesso!", "success");
      } catch (error) {
        console.error("Erro ao gerar PDF:", error);
        setStatus("Erro ao gerar o PDF. Verifique o console.", "error");
      }
    }

    document.getElementById("destNome").addEventListener("input", atualizarPreview);
    document.getElementById("remetenteNome").addEventListener("input", atualizarPreview);
    document.getElementById("remetenteCpfCnpj").addEventListener("input", atualizarPreview);
    document.getElementById("remetenteTelefone").addEventListener("input", atualizarPreview);
    document.getElementById("destRua").addEventListener("input", atualizarPreview);
    document.getElementById("destNumero").addEventListener("input", atualizarPreview);
    document.getElementById("destCidade").addEventListener("input", atualizarPreview);
    document.getElementById("destEstado").addEventListener("input", atualizarPreview);
    document.getElementById("destCep").addEventListener("input", atualizarPreview);
    document.getElementById("destRastreio").addEventListener("input", atualizarPreview);
    document.getElementById("peso").addEventListener("input", atualizarPreview);
    document.getElementById("embalagem").addEventListener("change", atualizarPreview);
    document.getElementById("servico").addEventListener("change", atualizarPreview);

    atualizarPreview();
  </script>
</body>
</html>