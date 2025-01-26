<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Feedback - Fonte dos Corais</title>
    <style>
        body {
            background-image: url(https://images.pexels.com/photos/4712763/pexels-photo-4712763.jpeg);
            background-size: cover; 
            background-position: center; 
            background-repeat: no-repeat; 
            height: 100%; 
            margin: 0; 
        }
        .container {
            width: 50%;
            margin: 50px auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h2 {
            text-align: center;
            color: #333;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            font-weight: bold;
            display: block;
            margin-bottom: 5px;
        }
        input[type="text"], input[type="email"], textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        textarea {
            height: 100px;
            resize: vertical;
        }
        .rating label {
            font-size: 20px;
            margin-right: 10px;
        }
        .rating input {
            display: none;
        }
        .rating input + label {
            cursor: pointer;
        }
        .rating input:checked ~ label {
            color: gold;
        }
        .btn-submit {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 4px;
            display: block;
            margin: 20px auto;
        }
        .btn-submit:hover {
            background-color: #45a049;
        }
        .container {
            width: 50%;
            margin: 50px auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h2 {
            text-align: center;
            color: #333;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            font-weight: bold;
            display: block;
            margin-bottom: 5px;
        }
        input[type="text"], input[type="email"], select, textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        textarea {
            height: 100px;
            resize: vertical;
        }
        .btn-submit {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 4px;
            display: block;
            margin: 20px auto;
        }
        .btn-submit:hover {
            background-color: #45a049;
        }
        .logo {
            width: 85px;
            height: 85px;
            border-radius: 70%;
            object-fit: cover;
            position: relative;
            top: 140px;
            left: 400px;
        }
    </style>
</head>
<body>
    <div>
        <img src="C:\Users\crazy\Downloads\Texto do seu parágrafo (3).png" alt="logo" class="logo">
        
    </div>

    <div class="container">
        <h2>Pesquisa de Feedback - Fonte dos Corais</h2>
        <form action="processa-feedback.php" method="POST">
            <div class="form-group">
                <label for="nome">Nome:</label>
                <input type="text" id="nome" name="nome" required>
            </div>
            
            <div class="form-group">
                <label for="email">E-mail:</label>
                <input type="email" id="email" name="email" required>
            </div>
            
            <div class="form-group">
                <label for="data-estadia">Data da Estadia:</label>
                <input type="text" id="data-estadia" name="data_estadia" placeholder="dd/mm/aaaa" required>
            </div>
            
            <div class="form-group">
                <label for="limpeza">Como você avaliaria a limpeza da pousada?</label>
                <select id="limpeza" name="limpeza" required>
                    <option value="Excelente">Excelente</option>
                    <option value="Boa">Boa</option>
                    <option value="Regular">Regular</option>
                    <option value="Ruim">Ruim</option>
                    <option value="Muito Ruim">Muito Ruim</option>
                </select>
            </div>
            
            <div class="form-group">
                <label for="atendimento">Como foi o atendimento dos funcionários?</label>
                <select id="atendimento" name="atendimento" required>
                    <option value="Excelente">Excelente</option>
                    <option value="Bom">Bom</option>
                    <option value="Regular">Regular</option>
                    <option value="Ruim">Ruim</option>
                </select>
            </div>

            <div class="form-group">
                <label for="atendimento">Como você conheceu nossa pousada?</label>
                <select id="atendimento" name="atendimento" required>
                    <option value="Excelente">Sou cliente antigo</option>
                    <option value="Bom">Busca na Internet</option>
                    <option value="Regular">Indicação de amigo</option>
                    <option value="Ruim">Redes Sociais</option>
                </select>
            </div>
            
            <div class="form-group">
                <label for="comodidade">As comodidades da pousada atenderam suas expectativas?</label>
                <select id="comodidade" name="comodidade" required>
                    <option value="Sim">Sim</option>
                    <option value="Não">Não</option>
                    <option value="Parcialmente">Parcialmente</option>
                </select>
            </div>
            
            <div class="form-group">
                <label for="localizacao">A localização da pousada foi conveniente para você?</label>
                <select id="localizacao" name="localizacao" required>
                    <option value="Sim">Sim</option>
                    <option value="Não">Não</option>
                </select>
            </div>
            
            <div class="form-group">
                <label for="recomendar">Você recomendaria esta pousada para outras pessoas?</label>
                <select id="recomendar" name="recomendar" required>
                    <option value="Sim">Sim</option>
                    <option value="Não">Não</option>
                </select>
            </div>

            <div class="form-group">
                <label for="comentarios">Comentários adicionais:</label>
                <textarea id="comentarios" name="comentarios" placeholder="Compartilhe suas experiências, sugestões ou críticas." required></textarea>
            </div>
            <div class="form-group rating">
                <label>Avaliação geral:</label>
                <input type="radio" id="star5" name="avaliacao" value="5"><label for="star5">★</label>
                <input type="radio" id="star4" name="avaliacao" value="4"><label for="star4">★</label>
                <input type="radio" id="star3" name="avaliacao" value="3"><label for="star3">★</label>
                <input type="radio" id="star2" name="avaliacao" value="2"><label for="star2">★</label>
                <input type="radio" id="star1" name="avaliacao" value="1"><label for="star1">★</label>
            </div>

            <button type="submit" class="btn-submit">Enviar Feedback</button>
        </form>
    </div>
</body>
</html>


<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $nome = $_POST['nome'];
    $feedback = $_POST['feedback'];

    $to = "crazyn2k05@gmail.com";
    $subject = "Novo Feedback";
    $message = "Nome: $nome\nFeedback: $feedback";
    $headers = "From: no-reply@seusite.com";

    mail($to, $subject, $message, $headers);
    echo "Feedback enviado com sucesso!";
}
?>
