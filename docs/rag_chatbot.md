<!-- Floating Chatbot Widget HTML & CSS -->
<div id="chatbot-container" style="display: none; position: fixed; bottom: 90px; right: 20px; width: 380px; height: 550px; background: white; border-radius: 12px; box-shadow: 0 5px 25px rgba(0,0,0,0.2); z-index: 9999; overflow: hidden; border: 1px solid #ddd;">

  <div style="display: flex; align-items: center; justify-content: space-between; padding-bottom: 12px; border-bottom: 1px solid #1e293b; margin-bottom: 20px;">
        <div style="display: flex; align-items: center; gap: 12px;">
            <div style="width: 36px; height: 36px; border-radius: 10px; background-color: rgba(13, 148, 136, 0.2); border: 1px solid rgba(13, 148, 136, 0.4); display: flex; align-items: center; justify-content: center; color: #2dd4bf;">
                🏛️
            </div>
            <div>
                <h3 style="margin: 0; font-size: 14px; font-weight: bold; color: white;">Apex Financial AI <span style="font-size: 10px; background-color: rgba(13, 148, 136, 0.2); color: #2dd4bf; padding: 2px 6px; border-radius: 4px; font-family: monospace;">RAG v2.4</span></h3>
                <p style="margin: 0; font-size: 11px; color: #94a3b8;">FastAPI backend • Qdrant embeddings</p>
            </div>
        </div>
      <button onclick="toggleChatbot()" style="background: none; border: none; color: white; font-size: 16px; cursor: pointer;">&times;</button>
    </div>
  
  <!-- <div style="background: #0e1117; color: white; padding: 10px 15px; display: flex; justify-content: space-between; align-items: center; font-family: sans-serif;">
    <span style="font-weight: bold; font-size: 14px;">🏛️ <span>Banking Assistant</span></span>
    <button onclick="toggleChatbot()" style="background: none; border: none; color: white; font-size: 16px; cursor: pointer;">&times;</button>
  </div> -->
  <!-- Streamlit embedded with embed=true parameter to strip extra toolbar headers -->
  <iframe src="https://yourfinbank.streamlit.app/?embed=true" style="width: 100%; height: calc(100% - 40px); border: none;"></iframe>
</div>

<!-- Floating Action Button (Bottom Right Corner) -->
<button onclick="toggleChatbot()" style="position: fixed; bottom: 20px; right: 20px; background-color: #ff4b4b; color: white; border: none; border-radius: 50px; padding: 12px 20px; font-size: 15px; font-weight: bold; cursor: pointer; box-shadow: 0 4px 12px rgba(0,0,0,0.3); z-index: 9998; display: flex; align-items: center; gap: 8px; font-family: sans-serif;">
  💬 Chat with AI
</button>

<!-- Optional: Inline Button to trigger it from text -->
<p>
  Have questions about my projects? <button onclick="toggleChatbot()" style="background: #ff4b4b; color: white; border: none; padding: 6px 12px; border-radius: 4px; cursor: pointer; font-weight: bold;">Open FinBank Chatbot</button>
</p>

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
