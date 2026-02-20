

# menopause-website
research
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Menopause Information - Accessible Website</title>

<style>
body {
    font-family: Arial, sans-serif;
    background-color: #000000;
    color: #FFFFFF;
    line-height: 1.6;
    font-size: 20px;
}

a {
    color: #00FFFF;
}

a:focus, button:focus {
    outline: 3px solid yellow;
}

header, nav, main, footer {
    padding: 20px;
}

button {
    font-size: 18px;
    padding: 10px;
    margin-top: 10px;
}

.skip-link {
    position: absolute;
    top: -40px;
    left: 0;
    background: yellow;
    color: black;
    padding: 8px;
}

.skip-link:focus {
    top: 0;
}
</style>
</head>

<body>

<a href="#maincontent" class="skip-link">Skip to Main Content</a>

<header role="banner">
    <h1>Understanding Menopause</h1>
</header>

<nav role="navigation" aria-label="Main Navigation">
    <ul>
        <li><a href="#what">What is Menopause?</a></li>
        <li><a href="#symptoms">Symptoms</a></li>
        <li><a href="#support">Support & Treatment</a></li>
    </ul>
</nav>

<main id="maincontent" role="main">

<section id="what">
    <h2>What is Menopause?</h2>
    <p>
        Menopause is a natural biological process that marks the end of menstrual cycles.
        It is diagnosed after 12 months without a period.
    </p>
</section>

<section id="symptoms">
    <h2>Common Symptoms</h2>
    <ul>
        <li>Hot flashes</li>
        <li>Night sweats</li>
        <li>Sleep problems</li>
        <li>Mood changes</li>
        <li>Vaginal dryness</li>
    </ul>
</section>

<section id="support">
    <h2>Support and Treatment Options</h2>
    <p>
        Treatments may include lifestyle changes, hormone therapy, or non-hormonal medications.
        Always consult a healthcare provider for medical advice.
    </p>

    <button onclick="readContent()">Read Page Aloud</button>
</section>

</main>

<footer role="contentinfo">
    <p>Accessible Menopause Information Website</p>
</footer>

<script>
function readContent() {
    const text = document.body.innerText;
    const speech = new SpeechSynthesisUtterance(text);
    speech.lang = "en-US";
    window.speechSynthesis.speak(speech);
}
</script>

</body>
</html>
