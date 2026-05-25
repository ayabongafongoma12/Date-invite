# Date-invite
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Our Date?</title>
<style>
  body { 
    background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    min-height: 100vh; display: flex; align-items: center; justify-content: center;
    font-family: 'Segoe UI', sans-serif; margin: 0; padding: 20px;
    color: #333; text-align: center;
  }
  .box {
    background: rgba(255,255,255,0.95); padding: 30px; border-radius: 20px;
    max-width: 500px; box-shadow: 0 8px 25px rgba(0,0,0,0.2);
  }
  h1 { color: #ff6b6b; margin-bottom: 15px; }
  p { font-size: 1.1em; margin-bottom: 20px; }
  a, button {
    display: inline-block; padding: 14px 30px; margin: 8px;
    background: #ff6b6b; color: #fff; text-decoration: none;
    border: none; border-radius: 50px; font-size: 1.1em; cursor: pointer;
  }
  http://a.no { background: #ccc; color: #333; }
  .food-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-top: 20px; }
  .food {
    background: #fff; border: 2px solid #ff6b6b; padding: 15px; border-radius: 15px;
    text-align: center; font-weight: bold;
    cursor: pointer;
    transition: all 0.3s;
  }
  .food:hover { background: #ff6b6b; color: #fff; transform: scale(1.05); }
  .food span { font-size: 2em; display: block; margin-bottom: 5px; }
  .final { font-size: 1.8em; color: #ff6b6b; font-weight: bold; }
  input[type=date] {
    padding: 12px; border-radius: 10px; border: 2px solid #ff6b6b; font-size: 1em;
    width: 80%; margin: 15px 0;
  }
</style>
</head>
<body>

<div class="box" id="page1">
  <h1>Will you go on a date with me? 🥺</h1>
  <p>I promise it'll be fun</p>
  <a href="#page2">Yes</a>
  <a href="#" class="no">No</a>
</div>

<div class="box" id="page2" style="display:none;">
  <h1>Pick a date 📅</h1>
  <p>When works for you?</p>
  <form onsubmit="event.preventDefault(); http://document.getElementById('page2').style.display='none'; http://document.getElementById('page3').style.display='block';">
    <input type="date" id="date" required>
    <br>
    <button type="submit">Next</button>
  </form>
</div>

<div class="box" id="page3" style="display:none;">
  <h1>Food we should get before going to watch the movie 🍽️</h1>
  <p>Choose your vibe</p>
  <div class="food-grid">
    <div class="food" onclick="finish('Steakhouse')">
      <span>🥩</span>
      Steakhouse
    </div>
    <div class="food" onclick="finish('Truffle Chicken')">
      <span>🍗</span>
      Truffle Chicken
    </div>
    <div class="food" onclick="finish('Wood-Fired Pizza')">
      <span>🍕</span>
      Wood-Fired Pizza
    </div>
    <div class="food" onclick="finish('Gourmet Burgers')">
      <span>🍔</span>
      Gourmet Burgers
    </div>
    <div class="food" onclick="finish('Italian Trattoria')">
      <span>🍝</span>
      Italian Trattoria
    </div>
    <div class="food" onclick="finish('French Bistro')">
      <span>🥖</span>
      French Bistro
    </div>
  </div>
</div>

<div class="box" id="page4" style="display:none;">
  <div class="final">
    Can't wait to see you<br>
    on <span id="pickedDate"></span><br>
    for <span id="pickedFood"></span><br>
    from Ayabonga ❤️
  </div>
</div>

<script>
function finish(food) {
  http://document.getElementById('pickedFood').textContent = food;
  http://document.getElementById('pickedDate').textContent = http://document.getElementById('date').value;
  http://document.getElementById('page3').style.display='none';
  http://document.getElementById('page4').style.display='block';
}
http://document.getElementById('noBtn')?.addEventListener('mouseover', () => {
  const btn = http://document.querySelector('a.no');
  const x = http://Math.random() _ (window.innerWidth - 100);
  const y = http://Math.random() _ (window.innerHeight - 100);
  http://btn.style.position = 'fixed';
  http://btn.style.left = x + 'px';
  http://btn.style.top = y + 'px';
});
</script>

</body>
</html>
