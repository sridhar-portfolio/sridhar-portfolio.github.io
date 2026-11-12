<div style="display: flex; flex-wrap: wrap; gap: 20px; align-items: center;">
  
  <!-- Left Side: Text -->
  <div style="flex: 1; min-width: 280px;">
    <h2>RAG-Produktassistent für das Bankwesen</h2>
	<p>Girokonten | Sparkonten | Kreditkarten | Privatkrediten | Mehr</p>
    <p>Hybrid-Index (Vektor- und Volltextsuche) über Finanzprodukt-Informationen, Gebührenverzeichnisse und Kreditrichtlinien. Inklusive Quellennachweis & Safety-Guardrails.</p>
	<button onclick="toggleChatbot()" class="button primary">
  		<i class="fa-solid fa-robot"></i> Try Live RAG Demo
	</button>
  </div>

  <!-- Right Side: Image -->
  <div style="flex: 1; min-width: 280px;">
    <img src="/assets/img/banks.jpg" alt="banks" style="width: 100%; height: auto; border-radius: 8px;" />
  </div>

</div>

---

## Features

### Portitor ullamcorper
Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.

### Sapien veroeros
Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.

### Quam lorem ipsum
Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.

### Sed magna finibus
Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.

<!-- Floating Chatbot Widget HTML & CSS -->
<div id="chatbot-container" style="display: none; position: fixed; bottom: 90px; right: 20px; width: 380px; height: 700px; background: white; border-radius: 12px; box-shadow: 0 5px 25px rgba(0,0,0,0.2); z-index: 9999; overflow: hidden; border: 1px solid #ddd;">
  	<div style="background: #0e1117; color: white; padding: 10px 15px; display: flex; justify-content: space-between; align-items: center; font-family: sans-serif;">
    	<span style="font-weight: bold; font-size: 14px;">🏛️ <span>Banking Assistant</span></span>
    	<button onclick="toggleChatbot()" style="background: none; border: none; color: white; font-size: 16px; cursor: pointer;">&times;</button>
  	</div>
  	<!-- Streamlit embedded with embed=true parameter to strip extra toolbar headers -->
  	<iframe src="https://yourfinbank.streamlit.app/?embed=true" style="width: 100%; height: calc(100% - 43px); border: none;"></iframe>
</div>

<!-- Floating Action Button (Bottom Right Corner) -->
<button onclick="toggleChatbot()" style="position: fixed; bottom: 20px; right: 20px; background-color: #ff4b4b; color: white; border: none; border-radius: 50px; padding: 12px 20px; font-size: 15px; font-weight: bold; cursor: pointer; box-shadow: 0 4px 12px rgba(0,0,0,0.3); z-index: 9998; display: flex; align-items: center; gap: 8px; font-family: sans-serif;">
  			<i class="fa-solid fa-robot"></i>
</button>
		
<!-- JavaScript to handle Open/Close toggle behavior -->
<script>
  function toggleChatbot() {
    const container = document.getElementById('chatbot-container');
    if (container.style.display === 'none' || container.style.display === '') {
      container.style.display = 'block';
    } else {
      container.style.display = 'none';
    }
  }
</script>






