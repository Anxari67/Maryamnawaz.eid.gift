# Maryamnawaz.eid.gift
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f9f9f9;
    color: #333;
    line-height: 1.6;
}
header {
    background-color: #2c3e50;
    color: white;
    padding: 30px 0;
    text-align: center;
}
header h1 {
    margin: 0;
    font-size: 2.5rem;
}
.counter {
    font-size: 1.5rem;
    font-weight: bold;
    margin-top: 10px;
    animation: fadeIn 2s ease-in-out;
}
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
.container {
    width: 90%;
    max-width: 600px;
    margin: 30px auto;
    background-color: white;
    padding: 25px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
}
h2 {
    font-size: 2rem;
    margin-bottom: 20px;
    color: #2c3e50;
}
form {
    display: flex;
    flex-direction: column;
}
form input {
    margin: 10px 0;
    padding: 12px;
    font-size: 16px;
    border: 1px solid #ddd;
    border-radius: 5px;
}
form button {
    padding: 12px;
    background-color: #2c3e50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
}
form button:hover {
    background-color: #34495e;
}
.popup {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: white;
    padding: 25px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    text-align: center;
    width: 90%;
    max-width: 400px;
}
.loading-bar {
    width: 100%;
    background-color: #ddd;
    margin: 15px 0;
    border-radius: 5px;
    overflow: hidden;
}
.loading-bar-progress {
    width: 0%;
    height: 20px;
    background-color: #2c3e50;
    transition: width 0.5s ease;
}
#shareButton {
    padding: 12px 20px;
    background-color: #25D366;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    margin-top: 15px;
}
#shareButton:hover {
    background-color: #128C7E;
}body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f9f9f9;
    color: #333;
    line-height: 1.6;
    background-image: url('maryam-nawaz.jpg'); /* Watermark image */
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    background-attachment: fixed;
    opacity: 0.9;
}
header {
    background-color: #2c3e50;
    color: white;
    padding: 30px 0;
    text-align: center;
}
header h1 {
    margin: 0;
    font-size: 2.5rem;
}
.counter {
    font-size: 1.5rem;
    font-weight: bold;
    margin-top: 10px;
    animation: fadeIn 2s ease-in-out;
}
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
.container {
    width: 90%;
    max-width: 600px;
    margin: 30px auto;
    background-color: rgba(255, 255, 255, 0.9);
    padding: 25px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
}
h2 {
    font-size: 2rem;
    margin-bottom: 20px;
    color: #2c3e50;
}
form {
    display: flex;
    flex-direction: column;
}
form input {
    margin: 10px 0;
    padding: 12px;
    font-size: 16px;
    border: 1px solid #ddd;
    border-radius: 5px;
}
form button {
    padding: 12px;
    background-color: #2c3e50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
}
form button:hover {
    background-color: #34495e;
}
.popup {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: white;
    padding: 25px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    text-align: center;
    width: 90%;
    max-width: 400px;
}
.loading-bar {
    width: 100%;
    background-color: #ddd;
    margin: 15px 0;
    border-radius: 5px;
    overflow: hidden;
}
.loading-bar-progress {
    width: 0%;
    height: 20px;
    background-color: #2c3e50;
    transition: width 0.5s ease;
}
#shareButton {
    padding: 12px 20px;
    background-color: #25D366;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    margin-top: 15px;
}
#shareButton:hover {
    background-color: #128C7E;
}
.footer-text {
    font-size: 14px;
    color: #555;
    text-align: center;
    margin-top: 20px;
}// Counter Logic
let counter = 87793; // Start with a large number
const counterElement = document.getElementById('counter');
setInterval(() => {
    counter += Math.floor(Math.random() * 100) + 50; // Increment by 50-150
    counterElement.textContent = counter.toLocaleString(); // Format number with commas
}, 3000); // Update every 3 seconds

// Form Submission Logic
const form = document.getElementById('giftForm');
const popup = document.getElementById('popup');
const loadingBar = document.getElementById('loadingBar');
const progressText = document.getElementById('progressText');
const shareButton = document.getElementById('shareButton');

form.addEventListener('submit', (e) => {
    e.preventDefault(); // Prevent form submission
    popup.style.display = 'block'; // Show popup
});

// Share Button Logic
let shareCount = 0;
const progressIncrements = [20, 35, 50, 65, 80, 95, 100]; // Progress increments for 7 clicks

shareButton.addEventListener('click', () => {
    if (shareCount === 0) {
        // Trigger ad on first click
        window.open('#', '_blank'); // Replace '#' with your ad link
    }

    // Update loading bar progress
    if (shareCount < progressIncrements.length) {
        const progress = progressIncrements[shareCount];
        loadingBar.style.width = `${progress}%`;
        progressText.textContent = `${progress}% Complete`;
        shareCount++;
    }

    // Open WhatsApp with pre-filled message
    const websiteURL = window.location.href;
    const message = `Maryam Nawaz is giving 20,000 as Eid gift. I received mine, now you receive yours. ${websiteURL}`;
    const whatsappURL = `https://wa.me/?text=${encodeURIComponent(message)}`;
    window.open(whatsappURL, '_blank');

    // Complete the process after 7 clicks
    if (shareCount === progressIncrements.length) {
        alert('Thank you for sharing! Your gift will be processed soon.');
        popup.style.display = 'none'; // Hide popup
    }
});
