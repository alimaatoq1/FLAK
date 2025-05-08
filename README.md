<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>FLAK</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    .container {
      display: flex;
      height: 100vh;
    }

    .left-panel {
      width: 30%;
      background-color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      padding: 40px;
      gap: 20px;
    }

    .link-button {
      background: none;
      border: none;
      color: black;
      font-size: 18px;
      display: flex;
      align-items: center;
      gap: 10px;
      cursor: pointer;
    }

    .link-button img {
      height: 24px;
    }

    .right-panel {
      width: 70%;
      background-color: black;
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 40px;
      text-align: center;
    }

    .flak-logo {
      width: 150px;
      margin-bottom: 20px;
    }

    #aboutButton {
      background-color: white;
      color: black;
      border: none;
      padding: 10px 20px;
      font-size: 18px;
      cursor: pointer;
    }

    #aboutText {
      margin-top: 30px;
      max-width: 700px;
      text-align: left;
      white-space: pre-wrap;
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="left-panel">
      <button class="link-button" onclick="window.open('https://www.instagram.com/flak_COMMUNITY/', '_blank')">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram"> Follow us on Instagram
      </button>
      <button class="link-button" onclick="window.open('https://discord.com/invite/rVU4H7mcwF', '_blank')">
        <img src="https://upload.wikimedia.org/wikipedia/commons/9/98/Discord_logo.svg" alt="Discord"> Join our Discord Server
      </button>
      <button class="link-button" onclick="window.open('https://www.guilded.gg/i/2Z1RDw9E', '_blank')">
        <img src="https://cdn.gilded.gg/icons/guilded-icon.svg" alt="Guilded"> Join our Guilded Server
      </button>
    </div>
    <div class="right-panel">
      <img src="https://cdn.discordapp.com/attachments/1365681695218466889/1365977300469944360/rumFZRb.png?ex=681dc57f&is=681c73ff&hm=d0a533cc715de1fb764287c4cb8ed1b3b4b3fa2887026536294802e4e6979bee&" alt="FLAK Logo" class="flak-logo">
      <button id="aboutButton">About Us</button>
      <div id="aboutText" class="hidden">
        Welcome to FLAK! We’re a community for gamers, friends, and anyone exploring new interests. Whether you’re playing, studying, or just hanging out, there’s a place for you here. With fun roles, helpful support, and tons to do, there’s always something new to discover. We’re glad you’re here!

        What You’ll Find at FLAK:

        💬 Chat Category
        • Hang out in General Chat for daily convos and random talks.
        • Dive into Gaming Chat to team up, share tips, or flex your wins.
        • Flex your gains or share fitness tips in Gym Chat.
        • Rev your engines in Car Chat — show off your rides, discuss mods, share car news, and everything automotive
        • Drop your best shots in Pics Chat — selfies, photography, artwork, anything visual.
        • Post the funniest content in our Memes Chat — because who doesn’t love a good meme?
        • Leveling system: the more you chat, the more perks you unlock!

        🗣️ Talking Category
        • Create your own custom VC whenever you want.
        • Personalize your hangout, bring your friends, vibe your way.

        🎬 Movies Category
        • Watching Together Stage for movie watch-alongs.
        • Two VC Channels for movie discussions.
        • Movie & Show Suggestions Forum.

        📚 Studying Category
        • Two Classroom Stages for study sessions and workshops.
        • Two Students’ Lounges (VCs) for casual studying.
        • Study-Topics Forum for sharing tips and organizing group studies.

        🎥 Streaming Category
        • Live Stage for recordings and streams.
        • Two VC Channels for gaming parties and live editing.
        • Stream & Content Suggestions Forum.

        At FLAK, we’re more than just a server — we’re a community where friendships form, passions grow, and good memories are made. No matter why you joined, you’re welcome here just as you are. This space is built by all of us, and now you’re part of the story too. We’re so glad you’re here — welcome to FLAK!
      </div>
    </div>
  </div>

  <script>
    document.getElementById('aboutButton').addEventListener('click', () => {
      const aboutText = document.getElementById('aboutText');
      aboutText.classList.toggle('hidden');
    });
  </script>
</body>
</html>
