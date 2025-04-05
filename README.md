# Site-de-reciclagem-em-HTML-bem-simples.
novato, cursando SENAI.

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reciclagem - Escola Marechal Rondon</title>
    <style>
        :root {
            --primary-color: #2E8B57;
            --secondary-color: #3CB371;
            --light-green: #E8F5E9;
            --dark-green: #1B5E20;
            --text-color: #333;
            --white: #FFFFFF;
            --shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: var(--text-color);
            line-height: 1.6;
        }
        
        .header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: var(--white);
            padding: 40px 20px;
            text-align: center;
            position: relative;
            box-shadow: var(--shadow);
        }
        
        .header h1 {
            margin: 0;
            font-size: 2.8em;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }
        
        .header p {
            font-size: 1.3em;
            margin-top: 15px;
            opacity: 0.9;
        }
        
        .container {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 20px;
        }
        
        .hero-image {
            width: 100%;
            height: 450px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 40px;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
            border: 5px solid var(--white);
        }
        
        .hero-image:hover {
            transform: scale(1.02);
        }
        
        .content-section {
            background-color: var(--white);
            padding: 35px;
            border-radius: 10px;
            margin-bottom: 50px;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
            border-left: 5px solid var(--secondary-color);
        }
        
        .content-section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.15);
        }
        
        .content-section h2 {
            color: var(--dark-green);
            border-bottom: 3px solid var(--secondary-color);
            padding-bottom: 12px;
            margin-top: 0;
            font-size: 2em;
        }
        
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }
        
        .gallery img {
            width: 100%;
            border-radius: 8px;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 3px 6px rgba(0,0,0,0.1);
        }
        
        .gallery img:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }
        
        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            margin: 40px 0;
            border-radius: 10px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }
        
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .menu {
            background-color: var(--dark-green);
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 50px;
            box-shadow: var(--shadow);
        }
        
        .menu h3 {
            color: var(--white);
            margin-top: 0;
            font-size: 1.6em;
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 12px;
            text-align: center;
        }
        
        .menu ul {
            list-style-type: none;
            padding: 0;
            margin: 20px 0 0 0;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 15px;
        }
        
        .menu li {
            margin-bottom: 12px;
            background-color: rgba(255,255,255,0.1);
            padding: 12px;
            border-radius: 6px;
            transition: background-color 0.3s;
        }
        
        .menu li:hover {
            background-color: rgba(255,255,255,0.2);
        }
        
        .menu a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s;
            font-size: 1.1em;
            display: block;
        }
        
        .menu a:hover {
            color: #C8E6C9;
        }
        
        .footer {
            background: linear-gradient(135deg, var(--dark-green), var(--primary-color));
            color: var(--white);
            text-align: center;
            padding: 30px;
            margin-top: 60px;
            box-shadow: 0 -4px 10px rgba(0,0,0,0.1);
        }
        
        .footer p {
            margin: 8px 0;
            font-size: 1.1em;
        }
        
        .author {
            font-style: italic;
            font-size: 1em;
            margin-top: 50px;
            text-align: center;
            color: #666;
            padding: 20px;
            background-color: var(--light-green);
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.05);
            border-top: 3px solid var(--secondary-color);
        }
        
        .recycling-methods {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        
        .method {
            background-color: var(--light-green);
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 3px 6px rgba(0,0,0,0.05);
            transition: transform 0.3s;
            border-left: 5px solid var(--secondary-color);
        }
        
        .method:hover {
            transform: translateY(-8px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.15);
        }
        
        .method h3 {
            color: var(--dark-green);
            margin-top: 0;
            font-size: 1.4em;
        }
        
        .method p {
            margin-bottom: 0;
        }
        
        .importance-list {
            list-style-type: none;
            padding: 0;
        }
        
        .importance-list li {
            margin-bottom: 15px;
            padding-left: 30px;
            position: relative;
            font-size: 1.1em;
        }
        
        .importance-list li:before {
            content: "✓";
            color: var(--secondary-color);
            font-weight: bold;
            position: absolute;
            left: 0;
            font-size: 1.3em;
        }
        
        .color-code {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 25px;
        }
        
        .color-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            background-color: var(--light-green);
            padding: 10px 15px;
            border-radius: 6px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }
        
        .color-box {
            width: 30px;
            height: 30px;
            border-radius: 6px;
            margin-right: 15px;
            border: 1px solid #ddd;
        }
        
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.2em;
            }
            
            .header p {
                font-size: 1.1em;
            }
            
            .content-section {
                padding: 25px;
            }
            
            .recycling-methods {
                grid-template-columns: 1fr;
            }
            
            .menu ul {
                grid-template-columns: 1fr;
            }
            
            .hero-image {
                height: 300px;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Reciclagem: Preservando Nosso Futuro</h1>
        <p>Projeto do Grêmio Estudantil da Escola Marechal Rondon - Ji-Paraná/RO</p>
    </div>
    
    <div class="container">
        <img src="https://www.portovelho.ro.gov.br/uploads/editor/capas/2024/02/1708624761ecoponto-parque-da-cidade-felipe-ribeiro-240222-00001.jpg" alt="Ecoponto em Ji-Paraná" class="hero-image">
        
        <div class="content-section" id="importancia">
            <h2>A Importância da Reciclagem</h2>
            <p>A reciclagem é um processo fundamental para a preservação do meio ambiente e a sustentabilidade do planeta. Através dela, transformamos materiais que seriam descartados como lixo em novos produtos, reduzindo a exploração de recursos naturais e diminuindo a poluição.</p>
            
            <p>Entre os principais benefícios da reciclagem estão:</p>
            <ul class="importance-list">
                <li>Redução da quantidade de lixo em aterros sanitários e lixões</li>
                <li>Economia de energia e recursos naturais</li>
                <li>Diminuição da poluição do ar, água e solo</li>
                <li>Geração de empregos na indústria da reciclagem</li>
                <li>Conscientização ambiental da população</li>
            </ul>
        </div>
        
        <div class="content-section" id="metodos">
            <h2>Métodos de Reciclagem</h2>
            <p>Existem diferentes métodos de reciclagem para cada tipo de material. Conheça os principais:</p>
            
            <div class="recycling-methods">
                <div class="method">
                    <h3>Reciclagem Mecânica</h3>
                    <p>Transformação física do resíduo em novos produtos. Comum para plásticos, metais e vidros. Representa cerca de 80% da reciclagem no Brasil.</p>
                </div>
                
                <div class="method">
                    <h3>Reciclagem Química</h3>
                    <p>Transformação molecular do material para produzir matéria-prima. Usada em plásticos complexos que não podem ser reciclados mecanicamente.</p>
                </div>
                
                <div class="method">
                    <h3>Reciclagem Energética</h3>
                    <p>Conversão do lixo em energia térmica ou elétrica através da incineração controlada. Requer cuidados com emissões de poluentes.</p>
                </div>
                
                <div class="method">
                    <h3>Compostagem</h3>
                    <p>Processo biológico de decomposição de matéria orgânica para produção de adubo. Reduz em até 50% o lixo doméstico.</p>
                </div>
            </div>
            
            <h3 style="margin-top: 40px;">Como Separar o Lixo Corretamente</h3>
            <p>No Brasil, utilizamos um sistema de cores para identificar os tipos de materiais recicláveis:</p>
            
            <div class="color-code">
                <div class="color-item">
                    <div class="color-box" style="background-color: #2F5597;"></div>
                    <span><strong>Azul:</strong> Papel e papelão</span>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #ED1C24;"></div>
                    <span><strong>Vermelho:</strong> Plásticos</span>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #22B14C;"></div>
                    <span><strong>Verde:</strong> Vidros</span>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #FFD700;"></div>
                    <span><strong>Amarelo:</strong> Metais</span>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #A67C52;"></div>
                    <span><strong>Marrom:</strong> Orgânicos</span>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #7F7F7F;"></div>
                    <span><strong>Cinza:</strong> Não recicláveis</span>
                </div>
            </div>
        </div>
        
        <div class="menu">
            <h3>Links Úteis sobre Reciclagem</h3>
            <ul>
                <li><a href="https://www.reciclasampa.com.br" target="_blank">Recicla Sampa - Informações sobre reciclagem</a></li>
                <li><a href="https://www.ecycle.com.br" target="_blank">eCycle - Como reciclar diversos materiais</a></li>
                <li><a href="https://www.cempre.org.br" target="_blank">CEMPRE - Compromisso Empresarial para Reciclagem</a></li>
                <li><a href="https://www.mma.gov.br" target="_blank">Ministério do Meio Ambiente</a></li>
                <li><a href="https://www.recicloteca.org.br" target="_blank">Recicloteca - Centro de Informações sobre Reciclagem</a></li>
                <li><a href="https://www.rondonia.ro.gov.br/meio-ambiente" target="_blank">SEMA Rondônia - Secretaria de Meio Ambiente</a></li>
                <li><a href="https://www.ji-parana.ro.gov.br" target="_blank">Prefeitura Municipal de Ji-Paraná</a></li>
            </ul>
        </div>
        
        <div class="content-section" id="ji-parana">
            <h2>Ativismos em Ji-Paraná, Rondônia</h2>
            <p>Em nossa cidade, diversas iniciativas promovem a reciclagem e a conscientização ambiental. Conheça algumas delas:</p>
            
            <div class="recycling-methods">
                <div class="method">
                    <h3>Projeto Recicla Ji-Paraná</h3>
                    <p>Iniciativa da prefeitura em parceria com cooperativas de catadores que já recolheu mais de 500 toneladas de materiais recicláveis desde 2020. Atua em todos os bairros da cidade.</p>
                </div>
                
                <div class="method">
                    <h3>Feira de Troca Sustentável</h3>
                    <p>Realizada mensalmente no Parque Ecológico, onde moradores podem trocar materiais recicláveis por produtos da cesta básica ou mudas de plantas. Já beneficiou mais de 1.000 famílias.</p>
                </div>
                
                <div class="method">
                    <h3>EcoPontos</h3>
                    <p>Pontos de coleta espalhados pela cidade para descarte correto de eletrônicos, pilhas, baterias e óleo de cozinha usado. Mais de 10 toneladas já foram coletadas.</p>
                </div>
            </div>
            
            <h3 style="margin-top: 40px;">Como Participar</h3>
            <p>Você pode contribuir com essas iniciativas de várias formas:</p>
            <ul class="importance-list">
                <li>Separando corretamente seus resíduos recicláveis</li>
                <li>Participando das feiras de troca sustentável</li>
                <li>Levando materiais especiais aos Ecopontos</li>
                <li>Divulgando as ações em suas redes sociais</li>
                <li>Voluntariando-se nos mutirões de limpeza</li>
            </ul>
        </div>
        
        <div class="author">
            <p>Projeto do Grêmio Estudantil da Escola Marechal Rondon - Ji-Paraná/RO</p>
            <p>03/04/2025</p>
        </div>
    </div>
    
    <div class="footer">
        <p>© 2025 Lucas Domingues Piovezan Vieira - Todos os direitos reservados</p>
        <p>Ji-Paraná - Rondônia</p>
        <p>Contato do criador: +55 69 9257-7149</p>
    </div>
</body>
</html>
