// Uruchomienie muzyki po załadowaniu strony
window.onload = function() {
    const music = document.getElementById("scaryMusic");
    music.play();
};

// Wyświetlanie wyskakujących okienek z komunikatem
function showPopup() {
    alert("Błąd! Wirus nie do usunięcia!");
}

// Pierwsze wyskakujące okienko po 3 sekundach
setTimeout(showPopup, 3000);

// Kolejne wyskakujące okienka co 5 sekund
setInterval(showPopup, 5000);

// Po 20 sekundach zmienia się treść strony na żart
setTimeout(function() {
    document.body.innerHTML = `
        <h1>To tylko żart!</h1>
        <p>Twoje dane są bezpieczne, nie masz wirusa!</p>
    `;
    const music = document.getElementById("scaryMusic");
    music.pause(); // Zatrzymanie muzyki
}, 20000); // Po 20 sekundach wyświetli się komunikat o ż
