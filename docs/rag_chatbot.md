<!DOCTYPE HTML>

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


<html>
	<head>
		<title>Editorial by HTML5 UP</title>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
		<link rel="stylesheet" href="assets/css/main.css" />
		<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
	</head>
	<body class="is-preload">
		<!-- Wrapper -->
			<div id="wrapper">
				<!-- Main -->
					<div id="main">
						<div class="inner">
							<!-- Header -->
								<header id="header">
									<a class="logo">Retrieval-Augmented Generation</a>
								</header>
							<!-- Banner -->
								<section id="banner">
									<div class="content">
										<header>
											<h1>RAG-Produktassistent für das Bankwesen</h1>
											<p>Girokonten | Sparkonten | Kreditkarten | Privatkrediten | Mehr</p>
										</header>
										<p>Hybrid-Index (Vektor- und Volltextsuche) über Finanzprodukt-Informationen, Gebührenverzeichnisse und Kreditrichtlinien. Inklusive Quellennachweis & Safety-Guardrails.</p>
										<ul class="actions">
											<li><button onclick="toggleChatbot()">
												<i class="fa-solid fa-robot"></i><span> Try Live RAG Demo</span></li>
											</button>
										</ul>
									</div>
									<span class="image object">
										<img src="/assets/img/banks.jpg" alt="banks" />
									</span>
								</section>
							<!-- Section -->
								<section>
									<header class="major">
										<h2>Features</h2>
									</header>
									<div class="features">
										<article>
											<span class="icon fa-gem"></span>
											<div class="content">
												<h3>Portitor ullamcorper</h3>
												<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
											</div>
										</article>
										<article>
											<span class="icon solid fa-paper-plane"></span>
											<div class="content">
												<h3>Sapien veroeros</h3>
												<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
											</div>
										</article>
										<article>
											<span class="icon solid fa-rocket"></span>
											<div class="content">
												<h3>Quam lorem ipsum</h3>
												<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
											</div>
										</article>
										<article>
											<span class="icon solid fa-signal"></span>
											<div class="content">
												<h3>Sed magna finibus</h3>
												<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
											</div>
										</article>
									</div>
								</section>
						</div>
					</div>
			</div>
		<!-- Scripts -->
			<script src="assets/js/jquery.min.js"></script>
			<script src="assets/js/browser.min.js"></script>
			<script src="assets/js/breakpoints.min.js"></script>
			<script src="assets/js/util.js"></script>
			<script src="assets/js/main.js"></script>
	</body>
</html>




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
