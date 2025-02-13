const actualBtn = document.getElementById('file-btn');
const fileChosen = document.getElementById('file-chosen');
actualBtn.addEventListener('change', function(){
    fileChosen.textContent = this.files[0].name
    })
const button = document.getElementById('btn');
button.addEventListener('click', () => {
    const targetSection = document.getElementById('section2');
    targetSection.scrollIntoView({
    behavior: 'smooth', // Smooth scrolling animation
    block: 'start'      // Scroll to the top of the target element
    });
});
const openPopupBtn = document.getElementById('openPopupBtn');
const closePopupBtn = document.getElementById('closePopupBtn');
const popupOverlay = document.getElementById('popupOverlay');
                
                        // Show the popup
openPopupBtn.addEventListener('click', () => {
    popupOverlay.style.display = 'flex'; // Use flex to center the content
    });
                
                        // Hide the popup
closePopupBtn.addEventListener('click', () => {
    popupOverlay.style.display = 'none';
    });
                
                        // Hide the popup when clicking outside the content
    popupOverlay.addEventListener('click', (event) => {
        if (event.target === popupOverlay) {
           popupOverlay.style.display = 'none';
            }
        });
window.addEventListener("load", () => {
    setTimeout(() => {
                        // Hide the loading section
    document.getElementById("loading-section").style.display = "none";
                        // Show the content section
    document.getElementById("home").style.display = "block";
    }, 3000); // 3-second delay
    });
const recognizedWordDiv = document.getElementById('recognizedWord');
const socket = new WebSocket('ws://localhost:5000');
                
socket.onmessage = function (event) {
const data = JSON.parse(event.data);
recognizedWordDiv.textContent = "Recognized Word: " + data.word;
}
