<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clínica de Estética e Podologia - Renata Silva</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        header {
            background-color: #f0a3c7;
            padding: 20px;
            text-align: center;
        }
        h1 {
            margin: 0;
        }
        .slogan {
            font-style: italic;
            color: #fff;
        }
        .contact {
            margin: 20px;
            text-align: center;
        }
        .contact input {
            padding: 10px;
            margin: 5px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            margin: 20px;
        }
        .gallery img {
            width: 150px;
            height: 150px;
            margin: 10px;
            border-radius: 5px;
            border: 1px solid #ddd;
        }
        .agenda {
            padding: 20px;
            text-align: center;
        }
        .month {
            display: none;
            margin: 20px auto;
            text-align: center;
        }
        .month.active {
            display: block;
        }
        .days {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 10px;
            margin: 10px;
        }
        .day {
            padding: 10px;
            background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: center;
            cursor: pointer;
        }
        .day:hover {
            background-color: #f0a3c7;
            color: white;
        }
        .navigation {
            margin: 20px;
        }
        .button {
            padding: 10px 20px;
            margin: 0 10px;
            border: none;
            border-radius: 5px;
            background-color: #f0a3c7;
            color: white;
            cursor: pointer;
        }
    </style>
    <script>
        let currentMonthIndex = 0;
        const months = ['janeiro', 'fevereiro', 'marco', 'abril', 'maio', 'junho', 'julho', 'agosto', 'setembro', 'outubro', 'novembro', 'dezembro'];

        function changeMonth(direction) {
            const monthsElements = document.querySelectorAll('.month');
            monthsElements[currentMonthIndex].classList.remove('active');
            currentMonthIndex += direction;

            if (currentMonthIndex < 0) {
                currentMonthIndex = 11; // volta para dezembro
            } else if (currentMonthIndex > 11) {
                currentMonthIndex = 0; // volta para janeiro
            }

            monthsElements[currentMonthIndex].classList.add('active');
        }

        function openAvailableHours(day) {
            const month = months[currentMonthIndex];
            const url = `horarios.html?date=${day}-${month}`;
            window.open(url, '_blank'); // Abre a página de horários
        }

        function goToCurrentMonth() {
            const monthsElements = document.querySelectorAll('.month');
            monthsElements.forEach((month, index) => {
                month.classList.remove('active');
                if (index === currentMonthIndex) {
                    month.classList.add('active');
                }
            });
        }
    </script>
</head>
<body>

<header>
    <h1>Clínica de Estética e Podologia</h1>
    <p class="slogan">Renata Silva</p>
</header>

<div class="contact">
    <h2>Contato</h2>
    <input type="text" placeholder="Telefone" value="+55 44 9835-4372" readonly />
    <input type="text" placeholder="Instagram" value="renatasilva_naildesigner" readonly />
</div>

<div class="gallery">
    <h2>Galeria</h2>
    <img src="https://via.placeholder.com/150" alt="Imagem 1" />
    <img src="https://via.placeholder.com/150" alt="Imagem 2" />
    <img src="https://via.placeholder.com/150" alt="Imagem 3" />
    <img src="https://via.placeholder.com/150" alt="Imagem 4" />
    <img src="https://via.placeholder.com/150" alt="Imagem 5" />
    <img src="https://via.placeholder.com/150" alt="Imagem 6" />
</div>

<div class="agenda">
    <h2>Agenda 2025</h2>
    <div class="navigation">
        <button class="button" onclick="changeMonth(-1)">Anterior</button>
        <button class="button" onclick="changeMonth(1)">Próximo</button>
    </div>
    <div id="months">
        <div class="month active" id="janeiro">
            <h3>Janeiro 2025</h3>
            <div class="days">
                <div class="day" onclick="openAvailableHours(1)">1</div>
                <div class="day" onclick="openAvailableHours(2)">2</div>
                <div class="day" onclick="openAvailableHours(3)">3</div>
                <div class="day" onclick="openAvailableHours(4)">4</div>
                <div class="day" onclick="openAvailableHours(5)">5</div>
                <div class="day" onclick="openAvailableHours(6)">6</div>
                <div class="day" onclick="openAvailableHours(7)">7</div>
                <div class="day" onclick="openAvailableHours(8)">8</div>
                <div class="day" onclick="openAvailableHours(9)">9</div>
                <div class="day" onclick="openAvailableHours(10)">10</div>
                <div class="day" onclick="openAvailableHours(11)">11</div>
                <div class="day" onclick="openAvailableHours(12)">12</div>
                <div class="day" onclick="openAvailableHours(13)">13</div>
                <div class="day" onclick="openAvailableHours(14)">14</div>
                <div class="day" onclick="openAvailableHours(15)">15</div>
                <div class="day" onclick="openAvailableHours(16)">16</div>
                <div class="day" onclick="openAvailableHours(17)">17</div>
                <div class="day" onclick="openAvailableHours(18)">18</div>
                <div class="day" onclick="openAvailableHours(19)">19</div>
                <div class="day" onclick="openAvailableHours(20)">20</div>
                <div class="day" onclick="openAvailableHours(21)">21</div>
                <div class="day" onclick="openAvailableHours(22)">22</div>
                <div class="day" onclick="openAvailableHours(23)">23</div>
                <div class="day" onclick="openAvailableHours(24)">24</div>
                <div class="day" onclick="openAvailableHours(25)">25</div>
                <div class="day" onclick="openAvailableHours(26)">26</div>
                <div class="day" onclick="openAvailableHours(27)">27</div>
                <div class="day" onclick="openAvailableHours(28)">28</div>
                <div class="day" onclick="openAvailableHours(29)">29</div>
                <div class="day" onclick="openAvailableHours(30)">30</div>
                <div class="day" onclick="openAvailableHours(31)">31</div>
            </div>
        </div>
        <div class="month" id="fevereiro">
            <h3>Fevereiro 2025</h3>
            <div class="days">
                <div class="day" onclick="openAvailableHours(1)">1</div>
                <div class="day" onclick="openAvailableHours(2)">2</div>
                <div class="day" onclick="openAvailableHours(3)">3</div>
                <div class="day" onclick="openAvailableHours(4)">4</div>
                <div class="day" onclick="openAvailableHours(5)">5</div>
                <div class="day" onclick="openAvailableHours(6)">6</div>
                <div class="day" onclick="openAvailableHours(7)">7</div>
                <div class="day" onclick="openAvailableHours(8)">8</div>
                <div class="day" onclick="openAvailableHours(9)">9</div>
                <div class="day" onclick="openAvailableHours(10)">10</div>
                <div class="day" onclick="openAvailableHours(11)">11</div>
                <div class="day" onclick="openAvailableHours(12)">12</div>
                <div class="day" onclick="openAvailableHours(13)">13</div>
                <div class="day" onclick="openAvailableHours(14)">14</div>
                <div class="day" onclick="openAvailableHours(15)">15</div>
                <div class="day" onclick="openAvailableHours(16)">16</div>
                <div class="day" onclick="openAvailableHours(17)">17</div>
                <div class="day" onclick="openAvailableHours(18)">18</div>
                <div class="day" onclick="openAvailableHours(19)">19</div>
                <div class="day" onclick="openAvailableHours(20)">20</div>
                <div class="day" onclick="openAvailableHours(21)">21</div>
                <div class="day" onclick="openAvailableHours(22)">22</div>
                <div class="day" onclick="openAvailableHours(23)">23</div>
                <div class="day" onclick="openAvailableHours(24)">24</div>
                <div class="day" onclick="openAvailableHours(25)">25</div>
                <div class="day" onclick="openAvailableHours(26)">26</div>
                <div class="day" onclick="openAvailableHours(27)">27</div>
                <div class="day" onclick="openAvailableHours(28)">28</div>
                <div class="day" onclick="openAvailableHours(29)">29</div>
            </div>
        </div>
        <!-- Continue para os outros meses -->
    </div>
</div>

</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Horários Disponíveis</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
        }
        h1 {
            text-align: center;
        }
        .hour {
            padding: 10px;
            margin: 5px;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: center;
            background-color: #f0a3c7;
            color: white;
            cursor: pointer;
        }
        .hour:hover {
            background-color: #d48aae;
        }
        .button {
            display: block;
            margin: 20px auto;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            background-color: #f0a3c7;
            color: white;
            cursor: pointer;
            text-align: center;
        }
        .button:hover {
            background-color: #d48aae;
        }

        /* Estilos do modal */
        .modal {
            display: none; /* Escondido por padrão */
            position: fixed; /* Fixo */
            z-index: 1; /* Fica na frente */
            left: 0;
            top: 0;
            width: 100%; /* Largura completa */
            height: 100%; /* Altura completa */
            overflow: auto; /* Habilita scroll se necessário */
            background-color: rgb(0,0,0); /* Cor de fundo */
            background-color: rgba(0,0,0,0.4); /* Fundo semi-transparente */
        }
        .modal-content {
            background-color: #fefefe;
            margin: 15% auto; /* 15% do topo e centralizado */
            padding: 20px;
            border: 1px solid #888;
            width: 80%; /* Largura do modal */
            text-align: center;
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }
        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>

<h1>Horários Disponíveis</h1>
<div id="available-hours"></div>

<button class="button" onclick="goBack()">Voltar à Tela Inicial</button>

<!-- Modal de seleção de horário -->
<div id="myModal" class="modal">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <p id="modal-text"></p>
        <button class="button" id="confirm-button">Confirmar Agendamento</button>
        <button class="button" onclick="closeModal()">Cancelar</button>
    </div>
</div>

<!-- Modal de confirmação -->
<div id="confirmModal" class="modal">
    <div class="modal-content">
        <span class="close" onclick="closeConfirmModal()">&times;</span>
        <p id="confirm-text"></p>
        <button class="button" onclick="closeConfirmModal()">Fechar</button>
    </div>
</div>

<script>
    const urlParams = new URLSearchParams(window.location.search);
    const date = urlParams.get('date');
    document.title = `Horários para ${date}`;

    const hoursContainer = document.getElementById('available-hours');
    const modal = document.getElementById("myModal");
    const confirmModal = document.getElementById("confirmModal");
    const modalText = document.getElementById("modal-text");
    const confirmText = document.getElementById("confirm-text");
    const confirmButton = document.getElementById("confirm-button");
    let selectedHour;

    for (let i = 9; i <= 19; i++) {
        const hourDiv = document.createElement('div');
        hourDiv.className = 'hour';
        hourDiv.textContent = `${i}:00`;
        hourDiv.onclick = function() {
            selectedHour = i; // Salva a hora selecionada
            modalText.textContent = `Você gostaria de agendar para ${i}:00 no dia ${date}?`;
            modal.style.display = "block"; // Mostra o modal
        };
        hoursContainer.appendChild(hourDiv);
    }

    function closeModal() {
        modal.style.display = "none"; // Esconde o modal
    }

    function closeConfirmModal() {
        confirmModal.style.display = "none"; // Esconde o modal de confirmação
    }

    confirmButton.onclick = function() {
        confirmText.textContent = `Agradecemos sua preferência! Agendamento confirmado para ${selectedHour}:00 no dia ${date}.`;
        confirmModal.style.display = "block"; // Mostra o modal de confirmação
        closeModal(); // Fecha o modal de seleção
    };

    function goBack() {
        window.location.href = "index.html"; // Substitua "index.html" pelo nome do seu arquivo de tela inicial
    }

    // Fecha o modal se o usuário clicar fora dele
    window.onclick = function(event) {
        if (event.target == modal) {
            closeModal();
        } else if (event.target == confirmModal) {
            closeConfirmModal();
        }
    }
</script>

</body>
</html>
