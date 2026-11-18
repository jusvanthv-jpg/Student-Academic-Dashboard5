# Student-Academic-Dashboard5
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Student Academic Dashboard</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background: #0b1020;
    color: white;
    display: flex;
    min-height: 100vh;
}

.sidebar {
    width: 240px;
    background: #131b32;
    padding: 25px 18px;
    min-height: 100vh;
}

.logo {
    font-size: 23px;
    font-weight: bold;
    color: #8b9cff;
    margin-bottom: 40px;
}

.sidebar a {
    display: block;
    color: #b7c2dc;
    padding: 15px;
    margin-bottom: 10px;
    text-decoration: none;
    border-radius: 10px;
}

.sidebar a:hover,
.sidebar a.active {
    background: #29375e;
    color: white;
}

.main {
    flex: 1;
    padding: 30px;
    min-width: 0;
}

.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
    margin-bottom: 30px;
}

.header h1 {
    font-size: 28px;
}

.header p {
    color: #9caac7;
    margin-top: 8px;
}

.profile {
    background: #202d4c;
    padding: 12px 20px;
    border-radius: 12px;
}

.cards {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
}

.card {
    background: #17223d;
    padding: 22px;
    border-radius: 16px;
    border: 1px solid #293958;
}

.card h3 {
    color: #aab7d2;
    font-size: 14px;
    margin-bottom: 15px;
}

.card h2 {
    font-size: 30px;
    color: #8c9fff;
}

.section {
    margin-top: 30px;
}

.section h2 {
    margin-bottom: 18px;
}

.content-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}

.panel {
    background: #17223d;
    padding: 22px;
    border-radius: 16px;
    border: 1px solid #293958;
}

.subject {
    margin: 20px 0;
}

.subject-info {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
}

.progress {
    height: 9px;
    background: #303d59;
    border-radius: 20px;
    overflow: hidden;
}

.bar {
    height: 100%;
    background: linear-gradient(90deg, #687cff, #a78bfa);
    border-radius: 20px;
}

.task {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    padding: 14px 0;
    border-bottom: 1px solid #34415c;
}

.task button {
    background: #687cff;
    border: none;
    padding: 8px 12px;
    color: white;
    border-radius: 7px;
    cursor: pointer;
}

.task.done span {
    text-decoration: line-through;
    color: #7f91ac;
}

.exam {
    padding: 14px;
    background: #202d4c;
    border-radius: 10px;
    margin-top: 12px;
}

input {
    padding: 11px;
    border: none;
    border-radius: 8px;
    width: 65%;
    margin-top: 12px;
}

.add-btn {
    padding: 11px 15px;
    border: none;
    border-radius: 8px;
    background: #687cff;
    color: white;
    cursor: pointer;
}

footer {
    text-align: center;
    color: #7f91ac;
    margin-top: 35px;
}

@media(max-width: 900px) {
    .cards {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width: 650px) {
    body {
        display: block;
    }

    .sidebar {
        width: 100%;
        min-height: auto;
        display: flex;
        overflow-x: auto;
        align-items: center;
        gap: 5px;
        padding: 10px;
    }

    .logo {
        margin: 0 12px 0 0;
        font-size: 18px;
    }

    .sidebar a {
        white-space: nowrap;
        margin: 0;
        padding: 10px;
    }

    .main {
        padding: 18px;
    }

    .cards,
    .content-grid {
        grid-template-columns: 1fr;
    }
}
</style>
</head>

<body>

<aside class="sidebar">
    <div class="logo">🎓 EduTrack</div>
    <a href="#dashboard" class="active">🏠 Dashboard</a>
    <a href="#subjects">📚 Subjects</a>
    <a href="#assignments">📝 Assignments</a>
    <a href="#exams">📅 Exams</a>
</aside>

<main class="main">

<header class="header" id="dashboard">
    <div>
        <h1>Student Dashboard 👋</h1>
        <p>Welcome back! Track your academic journey.</p>
    </div>
    <div class="profile">
        Jusvanth V | CSE AIML
    </div>
</header>

<section class="cards">
    <div class="card">
        <h3>Attendance</h3>
        <h2>92%</h2>
        <p>Overall attendance</p>
    </div>

    <div class="card">
        <h3>Assignments</h3>
        <h2 id="assignmentCount">3</h2>
        <p>Pending assignments</p>
    </div>

    <div class="card">
        <h3>Subjects</h3>
        <h2>6</h2>
        <p>Active subjects</p>
    </div>

    <div class="card">
        <h3>Study Hours</h3>
        <h2>24h</h2>
        <p>This week</p>
    </div>
</section>

<section class="section" id="subjects">
<h2>📊 Academic Performance</h2>

<div class="content-grid">
<div class="panel">

    <div class="subject">
        <div class="subject-info">
            <span>Mathematics</span><span>85%</span>
        </div>
        <div class="progress"><div class="bar" style="width:85%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Programming in C</span><span>90%</span>
        </div>
        <div class="progress"><div class="bar" style="width:90%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Artificial Intelligence</span><span>78%</span>
        </div>
        <div class="progress"><div class="bar" style="width:78%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Physics</span><span>82%</span>
        </div>
        <div class="progress"><div class="bar" style="width:82%"></div></div>
    </div>

</div>

<div class="panel" id="exams">
    <h2>📅 Upcoming Exams</h2>

    <div class="exam">
        <strong>Mathematics</strong>
        <p>20 November 2026</p>
    </div>

    <div class="exam">
        <strong>Programming in C</strong>
        <p>24 November 2026</p>
    </div>

    <div class="exam">
        <strong>Artificial Intelligence</strong>
        <p>28 November 2026</p>
    </div>
</div>
</div>
</section>

<section class="section" id="assignments">
<h2>📝 Assignment Tracker</h2>

<div class="panel">
    <div id="tasks">

        <div class="task">
            <span>Mathematics Assignment</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

        <div class="task">
            <span>C Programming Project</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

        <div class="task">
            <span>AI Seminar Preparation</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

    </div>

    <input id="newTask" type="text"
    placeholder="Enter a new assignment">

    <button class="add-btn" onclick="addTask()">
        + Add Task
    </button>
</div>
</section>

<footer>
    © 2026 EduTrack | Student Academic Management System
</footer>

</main>

<script>
function updateCount() {
    const tasks = document.querySelectorAll(
        '#tasks .task:not(.done)'
    );

    document.getElementById('assignmentCount')
    .textContent = tasks.length;
}

function completeTask(button) {
    const task = button.parentElement;

    task.classList.toggle('done');

    button.textContent = task.classList.contains('done')
        ? 'Undo'
        : 'Complete';

    updateCount();
}

function addTask() {
    const input = document.getElementById('newTask');
    const value = input.value.trim();

    if (value === '') {
        alert('Please enter an assignment!');
        return;
    }

    const task = document.createElement('div');
    task.className = 'task';

    const span = document.createElement('span');
    span.textContent = value;

    const button = document.createElement('button');
    button.textContent = 'Complete';
    button.onclick = function() {
        completeTask(this);
    };

    task.appendChild(span);
    task.appendChild(button);

    document.getElementById('tasks').appendChild(task);

    input.value = '';
    updateCount();
}

updateCount();
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Student Academic Dashboard</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background: #0b1020;
    color: white;
    display: flex;
    min-height: 100vh;
}

.sidebar {
    width: 240px;
    background: #131b32;
    padding: 25px 18px;
    min-height: 100vh;
}

.logo {
    font-size: 23px;
    font-weight: bold;
    color: #8b9cff;
    margin-bottom: 40px;
}

.sidebar a {
    display: block;
    color: #b7c2dc;
    padding: 15px;
    margin-bottom: 10px;
    text-decoration: none;
    border-radius: 10px;
}

.sidebar a:hover,
.sidebar a.active {
    background: #29375e;
    color: white;
}

.main {
    flex: 1;
    padding: 30px;
    min-width: 0;
}

.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
    margin-bottom: 30px;
}

.header h1 {
    font-size: 28px;
}

.header p {
    color: #9caac7;
    margin-top: 8px;
}

.profile {
    background: #202d4c;
    padding: 12px 20px;
    border-radius: 12px;
}

.cards {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
}

.card {
    background: #17223d;
    padding: 22px;
    border-radius: 16px;
    border: 1px solid #293958;
}

.card h3 {
    color: #aab7d2;
    font-size: 14px;
    margin-bottom: 15px;
}

.card h2 {
    font-size: 30px;
    color: #8c9fff;
}

.section {
    margin-top: 30px;
}

.section h2 {
    margin-bottom: 18px;
}

.content-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}

.panel {
    background: #17223d;
    padding: 22px;
    border-radius: 16px;
    border: 1px solid #293958;
}

.subject {
    margin: 20px 0;
}

.subject-info {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
}

.progress {
    height: 9px;
    background: #303d59;
    border-radius: 20px;
    overflow: hidden;
}

.bar {
    height: 100%;
    background: linear-gradient(90deg, #687cff, #a78bfa);
    border-radius: 20px;
}

.task {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    padding: 14px 0;
    border-bottom: 1px solid #34415c;
}

.task button {
    background: #687cff;
    border: none;
    padding: 8px 12px;
    color: white;
    border-radius: 7px;
    cursor: pointer;
}

.task.done span {
    text-decoration: line-through;
    color: #7f91ac;
}

.exam {
    padding: 14px;
    background: #202d4c;
    border-radius: 10px;
    margin-top: 12px;
}

input {
    padding: 11px;
    border: none;
    border-radius: 8px;
    width: 65%;
    margin-top: 12px;
}

.add-btn {
    padding: 11px 15px;
    border: none;
    border-radius: 8px;
    background: #687cff;
    color: white;
    cursor: pointer;
}

footer {
    text-align: center;
    color: #7f91ac;
    margin-top: 35px;
}

@media(max-width: 900px) {
    .cards {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width: 650px) {
    body {
        display: block;
    }

    .sidebar {
        width: 100%;
        min-height: auto;
        display: flex;
        overflow-x: auto;
        align-items: center;
        gap: 5px;
        padding: 10px;
    }

    .logo {
        margin: 0 12px 0 0;
        font-size: 18px;
    }

    .sidebar a {
        white-space: nowrap;
        margin: 0;
        padding: 10px;
    }

    .main {
        padding: 18px;
    }

    .cards,
    .content-grid {
        grid-template-columns: 1fr;
    }
}
</style>
</head>

<body>

<aside class="sidebar">
    <div class="logo">🎓 EduTrack</div>
    <a href="#dashboard" class="active">🏠 Dashboard</a>
    <a href="#subjects">📚 Subjects</a>
    <a href="#assignments">📝 Assignments</a>
    <a href="#exams">📅 Exams</a>
</aside>

<main class="main">

<header class="header" id="dashboard">
    <div>
        <h1>Student Dashboard 👋</h1>
        <p>Welcome back! Track your academic journey.</p>
    </div>
    <div class="profile">
        Jusvanth V | CSE AIML
    </div>
</header>

<section class="cards">
    <div class="card">
        <h3>Attendance</h3>
        <h2>92%</h2>
        <p>Overall attendance</p>
    </div>

    <div class="card">
        <h3>Assignments</h3>
        <h2 id="assignmentCount">3</h2>
        <p>Pending assignments</p>
    </div>

    <div class="card">
        <h3>Subjects</h3>
        <h2>6</h2>
        <p>Active subjects</p>
    </div>

    <div class="card">
        <h3>Study Hours</h3>
        <h2>24h</h2>
        <p>This week</p>
    </div>
</section>

<section class="section" id="subjects">
<h2>📊 Academic Performance</h2>

<div class="content-grid">
<div class="panel">

    <div class="subject">
        <div class="subject-info">
            <span>Mathematics</span><span>85%</span>
        </div>
        <div class="progress"><div class="bar" style="width:85%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Programming in C</span><span>90%</span>
        </div>
        <div class="progress"><div class="bar" style="width:90%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Artificial Intelligence</span><span>78%</span>
        </div>
        <div class="progress"><div class="bar" style="width:78%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Physics</span><span>82%</span>
        </div>
        <div class="progress"><div class="bar" style="width:82%"></div></div>
    </div>

</div>

<div class="panel" id="exams">
    <h2>📅 Upcoming Exams</h2>

    <div class="exam">
        <strong>Mathematics</strong>
        <p>20 November 2026</p>
    </div>

    <div class="exam">
        <strong>Programming in C</strong>
        <p>24 November 2026</p>
    </div>

    <div class="exam">
        <strong>Artificial Intelligence</strong>
        <p>28 November 2026</p>
    </div>
</div>
</div>
</section>

<section class="section" id="assignments">
<h2>📝 Assignment Tracker</h2>

<div class="panel">
    <div id="tasks">

        <div class="task">
            <span>Mathematics Assignment</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

        <div class="task">
            <span>C Programming Project</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

        <div class="task">
            <span>AI Seminar Preparation</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

    </div>

    <input id="newTask" type="text"
    placeholder="Enter a new assignment">

    <button class="add-btn" onclick="addTask()">
        + Add Task
    </button>
</div>
</section>

<footer>
    © 2026 EduTrack | Student Academic Management System
</footer>

</main>

<script>
function updateCount() {
    const tasks = document.querySelectorAll(
        '#tasks .task:not(.done)'
    );

    document.getElementById('assignmentCount')
    .textContent = tasks.length;
}

function completeTask(button) {
    const task = button.parentElement;

    task.classList.toggle('done');

    button.textContent = task.classList.contains('done')
        ? 'Undo'
        : 'Complete';

    updateCount();
}

function addTask() {
    const input = document.getElementById('newTask');
    const value = input.value.trim();

    if (value === '') {
        alert('Please enter an assignment!');
        return;
    }

    const task = document.createElement('div');
    task.className = 'task';

    const span = document.createElement('span');
    span.textContent = value;

    const button = document.createElement('button');
    button.textContent = 'Complete';
    button.onclick = function() {
        completeTask(this);
    };

    task.appendChild(span);
    task.appendChild(button);

    document.getElementById('tasks').appendChild(task);

    input.value = '';
    updateCount();
}

updateCount();
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Student Academic Dashboard</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background: #0b1020;
    color: white;
    display: flex;
    min-height: 100vh;
}

.sidebar {
    width: 240px;
    background: #131b32;
    padding: 25px 18px;
    min-height: 100vh;
}

.logo {
    font-size: 23px;
    font-weight: bold;
    color: #8b9cff;
    margin-bottom: 40px;
}

.sidebar a {
    display: block;
    color: #b7c2dc;
    padding: 15px;
    margin-bottom: 10px;
    text-decoration: none;
    border-radius: 10px;
}

.sidebar a:hover,
.sidebar a.active {
    background: #29375e;
    color: white;
}

.main {
    flex: 1;
    padding: 30px;
    min-width: 0;
}

.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
    margin-bottom: 30px;
}

.header h1 {
    font-size: 28px;
}

.header p {
    color: #9caac7;
    margin-top: 8px;
}

.profile {
    background: #202d4c;
    padding: 12px 20px;
    border-radius: 12px;
}

.cards {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
}

.card {
    background: #17223d;
    padding: 22px;
    border-radius: 16px;
    border: 1px solid #293958;
}

.card h3 {
    color: #aab7d2;
    font-size: 14px;
    margin-bottom: 15px;
}

.card h2 {
    font-size: 30px;
    color: #8c9fff;
}

.section {
    margin-top: 30px;
}

.section h2 {
    margin-bottom: 18px;
}

.content-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}

.panel {
    background: #17223d;
    padding: 22px;
    border-radius: 16px;
    border: 1px solid #293958;
}

.subject {
    margin: 20px 0;
}

.subject-info {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
}

.progress {
    height: 9px;
    background: #303d59;
    border-radius: 20px;
    overflow: hidden;
}

.bar {
    height: 100%;
    background: linear-gradient(90deg, #687cff, #a78bfa);
    border-radius: 20px;
}

.task {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    padding: 14px 0;
    border-bottom: 1px solid #34415c;
}

.task button {
    background: #687cff;
    border: none;
    padding: 8px 12px;
    color: white;
    border-radius: 7px;
    cursor: pointer;
}

.task.done span {
    text-decoration: line-through;
    color: #7f91ac;
}

.exam {
    padding: 14px;
    background: #202d4c;
    border-radius: 10px;
    margin-top: 12px;
}

input {
    padding: 11px;
    border: none;
    border-radius: 8px;
    width: 65%;
    margin-top: 12px;
}

.add-btn {
    padding: 11px 15px;
    border: none;
    border-radius: 8px;
    background: #687cff;
    color: white;
    cursor: pointer;
}

footer {
    text-align: center;
    color: #7f91ac;
    margin-top: 35px;
}

@media(max-width: 900px) {
    .cards {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width: 650px) {
    body {
        display: block;
    }

    .sidebar {
        width: 100%;
        min-height: auto;
        display: flex;
        overflow-x: auto;
        align-items: center;
        gap: 5px;
        padding: 10px;
    }

    .logo {
        margin: 0 12px 0 0;
        font-size: 18px;
    }

    .sidebar a {
        white-space: nowrap;
        margin: 0;
        padding: 10px;
    }

    .main {
        padding: 18px;
    }

    .cards,
    .content-grid {
        grid-template-columns: 1fr;
    }
}
</style>
</head>

<body>

<aside class="sidebar">
    <div class="logo">🎓 EduTrack</div>
    <a href="#dashboard" class="active">🏠 Dashboard</a>
    <a href="#subjects">📚 Subjects</a>
    <a href="#assignments">📝 Assignments</a>
    <a href="#exams">📅 Exams</a>
</aside>

<main class="main">

<header class="header" id="dashboard">
    <div>
        <h1>Student Dashboard 👋</h1>
        <p>Welcome back! Track your academic journey.</p>
    </div>
    <div class="profile">
        Jusvanth V | CSE AIML
    </div>
</header>

<section class="cards">
    <div class="card">
        <h3>Attendance</h3>
        <h2>92%</h2>
        <p>Overall attendance</p>
    </div>

    <div class="card">
        <h3>Assignments</h3>
        <h2 id="assignmentCount">3</h2>
        <p>Pending assignments</p>
    </div>

    <div class="card">
        <h3>Subjects</h3>
        <h2>6</h2>
        <p>Active subjects</p>
    </div>

    <div class="card">
        <h3>Study Hours</h3>
        <h2>24h</h2>
        <p>This week</p>
    </div>
</section>

<section class="section" id="subjects">
<h2>📊 Academic Performance</h2>

<div class="content-grid">
<div class="panel">

    <div class="subject">
        <div class="subject-info">
            <span>Mathematics</span><span>85%</span>
        </div>
        <div class="progress"><div class="bar" style="width:85%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Programming in C</span><span>90%</span>
        </div>
        <div class="progress"><div class="bar" style="width:90%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Artificial Intelligence</span><span>78%</span>
        </div>
        <div class="progress"><div class="bar" style="width:78%"></div></div>
    </div>

    <div class="subject">
        <div class="subject-info">
            <span>Physics</span><span>82%</span>
        </div>
        <div class="progress"><div class="bar" style="width:82%"></div></div>
    </div>

</div>

<div class="panel" id="exams">
    <h2>📅 Upcoming Exams</h2>

    <div class="exam">
        <strong>Mathematics</strong>
        <p>20 November 2026</p>
    </div>

    <div class="exam">
        <strong>Programming in C</strong>
        <p>24 November 2026</p>
    </div>

    <div class="exam">
        <strong>Artificial Intelligence</strong>
        <p>28 November 2026</p>
    </div>
</div>
</div>
</section>

<section class="section" id="assignments">
<h2>📝 Assignment Tracker</h2>

<div class="panel">
    <div id="tasks">

        <div class="task">
            <span>Mathematics Assignment</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

        <div class="task">
            <span>C Programming Project</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

        <div class="task">
            <span>AI Seminar Preparation</span>
            <button onclick="completeTask(this)">Complete</button>
        </div>

    </div>

    <input id="newTask" type="text"
    placeholder="Enter a new assignment">

    <button class="add-btn" onclick="addTask()">
        + Add Task
    </button>
</div>
</section>

<footer>
    © 2026 EduTrack | Student Academic Management System
</footer>

</main>

<script>
function updateCount() {
    const tasks = document.querySelectorAll(
        '#tasks .task:not(.done)'
    );

    document.getElementById('assignmentCount')
    .textContent = tasks.length;
}

function completeTask(button) {
    const task = button.parentElement;

    task.classList.toggle('done');

    button.textContent = task.classList.contains('done')
        ? 'Undo'
        : 'Complete';

    updateCount();
}

function addTask() {
    const input = document.getElementById('newTask');
    const value = input.value.trim();

    if (value === '') {
        alert('Please enter an assignment!');
        return;
    }

    const task = document.createElement('div');
    task.className = 'task';

    const span = document.createElement('span');
    span.textContent = value;

    const button = document.createElement('button');
    button.textContent = 'Complete';
    button.onclick = function() {
        completeTask(this);
    };

    task.appendChild(span);
    task.appendChild(button);

    document.getElementById('tasks').appendChild(task);

    input.value = '';
    updateCount();
}

updateCount();
</script>

</body>
</html>
