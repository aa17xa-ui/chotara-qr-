# chotara-qr-<div id="container" style="text-align: center; background: #FFF0F5; padding: 50px; border-radius: 20px;">
    <button id="playButton" style="padding: 20px 40px; font-size: 20px; background: #FF69B4; color: white; border: none; border-radius: 50px; cursor: pointer;">
        Click for a Surprise! ✨
    </button>
    
    <img id="finalPhoto" src="YOUR_PHOTO_URL" style="display: none; width: 100%; max-width: 400px; border-radius: 15px; margin-top: 20px;">
</div>

<script>
    let stage = 0;
    const audio1 = new Audio('YOUR_AUDIO_1_URL'); // Sentence 1.mp3
    const audio2 = new Audio('YOUR_AUDIO_2_URL'); // Sentence 2.mp3
    const btn = document.getElementById('playButton');
    const img = document.getElementById('finalPhoto');

    btn.onclick = function() {
        stage++;
        if (stage === 1) {
            audio1.play();
            btn.innerHTML = "Again! 😋";
        } else if (stage === 2) {
            audio2.play();
            btn.innerHTML = "One last time... 🕷️";
        } else if (stage === 3) {
            btn.style.display = 'none';
            img.style.display = 'block';
        }
    };
</script>
