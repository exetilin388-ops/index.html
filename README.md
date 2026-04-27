<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Past Tense</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #eef2f3; }
    header { background: #1e3a5f; color: white; padding: 20px; text-align: center; }
    section { padding: 20px; margin: 15px; background: white; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    h2 { color: #1e3a5f; }
    input { padding: 8px; margin: 5px 0 10px 0; width: 100%; }
    button { background: #3498db; color: white; border: none; padding: 10px 15px; cursor: pointer; border-radius: 5px; margin-top:10px; }
    .option { margin: 5px 0; }
  </style>
</head>
<body><header>
  <h1>Simple Past Tense</h1>
  <p>Learn Regular and Irregular Verbs</p>
</header><section>
  <h2>What is Simple Past?</h2>
  <p>The simple past tense is used to describe actions that started and finished in the past.</p>
  <ul>
    <li>I visited my grandma yesterday.</li>
    <li>She watched a movie last night.</li>
    <li>We played soccer on Sunday.</li>
  </ul>
</section><section>
  <h2>Regular Verbs</h2>
  <p>Regular verbs add <b>-ed</b>.</p>
  <ul>
    <li>Play → Played</li>
    <li>Work → Worked</li>
    <li>Clean → Cleaned</li>
    <li>Visit → Visited</li>
  </ul>
</section><section>
  <h2>Irregular Verbs</h2>
  <p>No rule, they change form.</p>
  <ul>
    <li>Go → Went</li>
    <li>Eat → Ate</li>
    <li>See → Saw</li>
    <li>Buy → Bought</li>
  </ul>
</section><section>
  <h2>Write the Past Form</h2>
  <label>1. Play:</label>
  <input id="q1">
  <label>2. Go:</label>
  <input id="q2">
  <label>3. Eat:</label>
  <input id="q3">
  <label>4. Work:</label>
  <input id="q4">
  <button onclick="checkAnswers()">Check</button>
  <p id="result"></p>
</section><section>
  <h2>Multiple Choice</h2>  <p>1. She ___ to school yesterday.</p>
  <div class="option"><input type="radio" name="m1" value="goed"> Goed</div>
  <div class="option"><input type="radio" name="m1" value="went"> Went</div>
  <div class="option"><input type="radio" name="m1" value="goes"> Goes</div>  <p>2. They ___ a movie last night.</p>
  <div class="option"><input type="radio" name="m2" value="watch"> Watch</div>
  <div class="option"><input type="radio" name="m2" value="watched"> Watched</div>
  <div class="option"><input type="radio" name="m2" value="watching"> Watching</div>  <p>3. He ___ pizza yesterday.</p>
  <div class="option"><input type="radio" name="m3" value="eat"> Eat</div>
  <div class="option"><input type="radio" name="m3" value="ate"> Ate</div>
  <div class="option"><input type="radio" name="m3" value="eated"> Eated</div><button onclick="checkMC()">Check Multiple Choice</button>

  <p id="mcResult"></p>
</section><script>
function checkAnswers() {
  let score = 0;
  if(document.getElementById('q1').value.toLowerCase() === 'played') score++;
  if(document.getElementById('q2').value.toLowerCase() === 'went') score++;
  if(document.getElementById('q3').value.toLowerCase() === 'ate') score++;
  if(document.getElementById('q4').value.toLowerCase() === 'worked') score++;
  document.getElementById('result').innerText = 'Score: ' + score + '/4';
}

function checkMC() {
  let score = 0;
  if(document.querySelector('input[name="m1"]:checked')?.value === 'went') score++;
  if(document.querySelector('input[name="m2"]:checked')?.value === 'watched') score++;
  if(document.querySelector('input[name="m3"]:checked')?.value === 'ate') score++;
  document.getElementById('mcResult').innerText = 'Multiple Choice Score: ' + score + '/3';
}
</script></body>
</html>
