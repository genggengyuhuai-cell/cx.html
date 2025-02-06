<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI工程师成长路线图</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --primary: #2c3e50;
            --accent: #e74c3c;
            --bg: #f8f9fa;
        }
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: 'Segoe UI', system-ui;
            line-height: 1.6;
            background: var(--bg);
            padding: 20px;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* 打卡面板 */
        .daily-check {
            background: white;
            padding: 1.5rem;
            border-radius: 12px;
            margin-bottom: 2rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }
        .calendar {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 5px;
            margin-top: 1rem;
        }
        .day {
            padding: 10px;
            text-align: center;
            border-radius: 8px;
            background: #eee;
            cursor: pointer;
        }
        .day.checked {
            background: var(--accent);
            color: white;
        }

        /* 学习阶段 */
        .phase {
            background: white;
            border-radius: 12px;
            padding: 1.5rem;
            margin: 2rem 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            position: relative;
        }
        .phase::before {
            content: '';
            position: absolute;
            left: -30px;
            top: 20px;
            width: 20px;
            height: 20px;
            background: var(--accent);
            border-radius: 50%;
        }
        h2 {
            color: var(--primary);
            margin: 1rem 0;
            display: flex;
            align-items: center;
        }
        .progress {
            height: 8px;
            background: #eee;
            border-radius: 4px;
            margin: 1rem 0;
        }
        .progress-bar {
            height: 100%;
            background: var(--accent);
            width: 0;
            transition: width 0.3s ease;
        }

        /* 任务系统 */
        .task-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1rem;
        }
        .task-card {
            padding: 1rem;
            border: 1px solid #eee;
            border-radius: 8px;
        }
        .task-list {
            list-style: none;
            padding: 0;
        }
        .task-item {
            padding: 0.8rem;
            margin: 0.5rem 0;
            background: var(--bg);
            border-left: 3px solid var(--accent);
            display: flex;
            align-items: center;
        }
        input[type="checkbox"] {
            margin-right: 1rem;
            transform: scale(1.2);
        }

        /* 资源库 */
        .resource-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }
        .resource-card {
            padding: 1rem;
            background: var(--bg);
            border-radius: 8px;
        }
        .resource-card a {
            color: var(--primary);
            text-decoration: none;
        }
        .resource-card a:hover {
            text-decoration: underline;
        }
        .tag {
            display: inline-block;
            padding: 0.2rem 0.5rem;
            background: #e74c3c20;
            color: #e74c3c;
            border-radius: 4px;
            font-size: 0.8rem;
            margin: 0.3rem 0;
        }

        @media (max-width: 768px) {
            .phase { margin-left: 20px; }
            .phase::before { left: -20px; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 每日打卡 -->
        <div class="daily-check">
            <h2><i class="fas fa-calendar-check"></i> 学习打卡日历</h2>
            <div class="calendar" id="calendar"></div>
        </div>

        <!-- 基础筑基阶段 -->
        <div class="phase">
            <h2><i class="fas fa-tools"></i> 基础筑基阶段 (2024.09-2024.10)</h2>
            <div class="progress">
                <div class="progress-bar" style="width: 25%"></div>
            </div>
            
            <div class="task-grid">
                <div class="task-card">
                    <h3>📅 学习任务</h3>
                    <ul class="task-list">
                        <li class="task-item"><input type="checkbox"> Python语法强化</li>
                        <li class="task-item"><input type="checkbox"> Numpy/Pandas实战</li>
                        <li class="task-item"><input type="checkbox"> Kaggle入门竞赛</li>
                    </ul>
                </div>
                <div class="task-card">
                    <h3>📚 学习资源</h3>
                    <div class="resource-grid">
                        <div class="resource-card">
                            <div class="tag">书籍</div>
                            <ul>
                                <li><a href="https://book.douban.com/subject/35069199/">《Python编程》</a></li>
                                <li><a href="https://hands1ml.apachecn.org/">《Hands-On ML》</a></li>
                            </ul>
                        </div>
                        <div class="resource-card">
                            <div class="tag">课程</div>
                            <ul>
                                <li><a href="https://www.coursera.org/learn/machine-learning">吴恩达ML</a></li>
                                <li><a href="https://www.kaggle.com/learn">Kaggle微课</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 其他阶段结构相同... -->

    </div>

    <script>
        // 打卡系统
        function generateCalendar() {
            const calendar = document.getElementById('calendar');
            const today = new Date();
            
            for (let i = 0; i < 30; i++) {
                const day = document.createElement('div');
                day.className = 'day';
                day.textContent = i + 1;
                
                // 从localStorage读取打卡状态
                if(localStorage.getItem(`day-${i+1}`)) {
                    day.classList.add('checked');
                }

                day.addEventListener('click', () => {
                    day.classList.toggle('checked');
                    localStorage.setItem(`day-${i+1}`, day.classList.contains('checked'));
                });
                
                calendar.appendChild(day);
            }
        }

        // 任务进度系统
        document.querySelectorAll('.phase').forEach(phase => {
            const checkboxes = phase.querySelectorAll('input[type="checkbox"]');
            const progressBar = phase.querySelector('.progress-bar');
            
            checkboxes.forEach(checkbox => {
                // 加载保存状态
                const storageKey = `task-${phase.id}-${checkbox.nextSibling.textContent.trim()}`;
                if(localStorage.getItem(storageKey)) {
                    checkbox.checked = true;
                    updateProgress();
                }

                checkbox.addEventListener('change', () => {
                    localStorage.setItem(storageKey, checkbox.checked);
                    updateProgress();
                });
            });

            function updateProgress() {
                const checked = phase.querySelectorAll('input:checked').length;
                const total = checkboxes.length;
                const progress = (checked / total * 100).toFixed(0);
                progressBar.style.width = progress + '%';
            }
        });

        // 初始化
        generateCalendar();
    </script>
</body>
</html>
