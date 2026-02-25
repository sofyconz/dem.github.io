<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Решение криптарифметических ребусов</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            padding: 20px;
            min-height: 100vh;
            color: #eee;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: #1a253a;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.5);
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(135deg, #00b4db 0%, #0083b0 100%);
            color: white;
            padding: 30px;
            text-align: center;
        }
        
        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        
        .header .date {
            font-size: 1.2em;
            opacity: 0.9;
        }
        
        .content {
            padding: 30px;
        }
        
        .puzzle {
            background: #24344d;
            border-left: 5px solid #00b4db;
            border-radius: 10px;
            padding: 25px;
            margin-bottom: 25px;
            transition: transform 0.3s ease;
        }
        
        .puzzle:hover {
            transform: translateX(5px);
            box-shadow: 0 5px 20px rgba(0, 180, 219, 0.3);
        }
        
        .puzzle h2 {
            color: #00b4db;
            margin-bottom: 15px;
            font-size: 1.5em;
        }
        
        .status {
            display: inline-block;
            background: #00d26a;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9em;
            margin-bottom: 15px;
        }
        
        .mapping {
            background: #1a253a;
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .mapping-item {
            background: linear-gradient(135deg, #00b4db 0%, #0083b0 100%);
            color: white;
            padding: 8px 15px;
            border-radius: 5px;
            font-weight: bold;
        }
        
        .calculation {
            background: #0d1117;
            color: #00ff88;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Courier New', monospace;
            font-size: 1.1em;
            white-space: pre;
            overflow-x: auto;
            border: 2px solid #00d26a;
        }
        
        .result {
            background: linear-gradient(135deg, #00d26a 0%, #00b4db 100%);
            color: white;
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            font-size: 1.2em;
            margin-top: 15px;
        }
        
        .summary {
            background: linear-gradient(135deg, #00b4db 0%, #0083b0 100%);
            color: white;
            padding: 25px;
            border-radius: 10px;
            text-align: center;
            margin-top: 30px;
        }
        
        .summary table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
            background: #1a253a;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .summary th {
            background: #0083b0;
            color: white;
            padding: 12px;
        }
        
        .summary td {
            padding: 12px;
            color: #eee;
            border-bottom: 1px solid #24344d;
        }
        
        .summary tr:last-child td {
            border-bottom: none;
        }
        
        .summary tr:hover {
            background: #24344d;
        }
        
        .download-links {
            background: #24344d;
            padding: 20px;
            text-align: center;
            border-radius: 10px;
            margin-bottom: 20px;
            border: 2px solid #00b4db;
        }
        
        .download-links a {
            color: #00ff88;
            text-decoration: none;
            margin: 0 10px;
            font-weight: bold;
        }
        
        .download-links a:hover {
            color: #00b4db;
            text-decoration: underline;
        }
        
        .emoji {
            font-size: 1.3em;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🧩 Решение криптарифметических ребусов</h1>
            <p class="date">📅 Дата: 25.02.2026</p>
        </div>
        
        <div class="content">
            <div class="download-links">
                <p>📎 Файлы для скачивания:</p>
                <a href="presentation.pptx">📊 Презентация (PPTX)</a> • 
                <a href="index.html">🌐 Проверка кириллицы (HTML)</a>
            </div>

            <!-- Ребус 1 -->
            <div class="puzzle">
                <h2>1️⃣ SEND + MORE = MONEY</h2>
                <span class="status">✅ Решение найдено!</span>
                
                <div class="mapping">
                    <span class="mapping-item">S = 9</span>
                    <span class="mapping-item">E = 5</span>
                    <span class="mapping-item">N = 6</span>
                    <span class="mapping-item">D = 7</span>
                    <span class="mapping-item">M = 1</span>
                    <span class="mapping-item">O = 0</span>
                    <span class="mapping-item">R = 8</span>
                    <span class="mapping-item">Y = 2</span>
                </div>
                
                <div class="calculation">
    9 5 6 7   (SEND)
+   1 0 8 5   (MORE)
───────────
  1 0 6 5 2   (MONEY)</div>
                
                <div class="result">
                    ✅ 9567 + 1085 = 10652
                </div>
            </div>

            <!-- Ребус 2 -->
            <div class="puzzle">
                <h2>2️⃣ ВОЛК + ЛИСА = ЗВЕРИ</h2>
                <span class="status">✅ Решение найдено</span>
                
                <div class="mapping">
                    <span class="mapping-item">В = 5</span>
                    <span class="mapping-item">О = 3</span>
                    <span class="mapping-item">Л = 9</span>
                    <span class="mapping-item">К = 4</span>
                    <span class="mapping-item">И = 6</span>
                    <span class="mapping-item">С = 8</span>
                    <span class="mapping-item">А = 2</span>
                    <span class="mapping-item">З = 1</span>
                    <span class="mapping-item">Е = 0</span>
                    <span class="mapping-item">Р = 7</span>
                </div>
                
                <div class="calculation">
    5 3 9 4   (ВОЛК)
+   9 6 8 2   (ЛИСА)
───────────
  1 5 0 7 6   (ЗВЕРИ)</div>
                
                <div class="result">
                    ✅ 5,394 + 9,682 = 15,076
                </div>
            </div>

            <!-- Ребус 3 -->
            <div class="puzzle">
                <h2>3️⃣ КТО + КОТ = ТОК</h2>
                <span class="status">✅ Решение найдено</span>
                
                <div class="mapping">
                    <span class="mapping-item">К = 4</span>
                    <span class="mapping-item">Т = 9</span>
                    <span class="mapping-item">О = 5</span>
                </div>
                
                <div class="calculation">
    4 9 5   (КТО)
+   4 5 9   (КОТ)
─────────
    9 5 4   (ТОК)</div>
                
                <div class="result">
                    ✅ 495 + 459 = 954
                </div>
            </div>

            <!-- Ребус 4 -->
            <div class="puzzle">
                <h2>4️⃣ КОШКА + КОШКА + КОШКА = СОБАКА</h2>
                <span class="status">✅ Решение найдено</span>
                
                <div class="mapping">
                    <span class="mapping-item">К = 5</span>
                    <span class="mapping-item">О = 7</span>
                    <span class="mapping-item">Ш = 3</span>
                    <span class="mapping-item">А = 0</span>
                    <span class="mapping-item">С = 1</span>
                    <span class="mapping-item">Б = 2</span>
                </div>
                
                <div class="calculation">
    5 7 3 5 0   (КОШКА)
    5 7 3 5 0   (КОШКА)
+   5 7 3 5 0   (КОШКА)
─────────────
  1 7 2 0 5 0   (СОБАКА)</div>
                
                <div class="result">
                    ✅ 57,350 × 3 = 172,050
                </div>
            </div>

            <!-- Ребус 5 -->
            <div class="puzzle">
                <h2>5️⃣ СИНУС + СИНУС + КОСИНУС = ТАНГЕНС</h2>
                <span class="status">✅ Решение найдено</span>
                
                <div class="mapping">
                    <span class="mapping-item">С = 5</span>
                    <span class="mapping-item">И = 8</span>
                    <span class="mapping-item">Н = 7</span>
                    <span class="mapping-item">У = 2</span>
                    <span class="mapping-item">К = 3</span>
                    <span class="mapping-item">О = 9</span>
                    <span class="mapping-item">Т = 4</span>
                    <span class="mapping-item">А = 0</span>
                    <span class="mapping-item">Г = 6</span>
                    <span class="mapping-item">Е = 1</span>
                </div>
                
                <div class="calculation">
      5 8 7 2 5   (СИНУС)
      5 8 7 2 5   (СИНУС)
+ 3 9 5 8 7 2 5   (КОСИНУС)
─────────────────
  4 0 7 6 1 7 5   (ТАНГЕНС)</div>
                
                <div class="result">
                    ✅ 58,725 + 58,725 + 3,958,725 = 4,076,175
                </div>
            </div>

            <!-- Итоговая сводка -->
            <div class="summary">
                <h2>📊 Итоговая сводка</h2>
                <table>
                    <thead>
                        <tr>
                            <th>№</th>
                            <th>Ребус</th>
                            <th>Статус</th>
                            <th>Результат</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>SEND + MORE = MONEY</td>
                            <td>✅</td>
                            <td>9567 + 1085 = 10652</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>ВОЛК + ЛИСА = ЗВЕРИ</td>
                            <td>✅</td>
                            <td>5394 + 9682 = 15076</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>КТО + КОТ = ТОК</td>
                            <td>✅</td>
                            <td>495 + 459 = 954</td>
                        </tr>
                        <tr>
                            <td>4</td>
                            <td>КОШКА × 3 = СОБАКА</td>
                            <td>✅</td>
                            <td>57350 × 3 = 172050</td>
                        </tr>
                        <tr>
                            <td>5</td>
                            <td>СИНУС×2 + КОСИНУС = ТАНГЕНС</td>
                            <td>✅</td>
                            <td>58725×2 + 3958725 = 4076175</td>
                        </tr>
                    </tbody>
                </table>
                
                <div style="margin-top: 20px; font-size: 1.5em;">
                    🏆 <strong>Все 5 ребусов успешно решены!</strong>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
