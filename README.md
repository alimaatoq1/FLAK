<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
 
  <style>
    body {
      background-color: #0a0a0a;
      color: #ffffff;
      font-family: 'Arial', sans-serif;
      text-align: center;
      padding: 50px;
    }

    #flak-logo {
      width: 150px; /* Adjust size */
      margin-bottom: 30px;
    }

    h1 {
      font-size: 3em;
      margin-bottom: 20px;
    }

    button {
      background-color: #00ffff;
      border: none;
      padding: 15px 30px;
      font-size: 1.2em;
      cursor: pointer;
      color: #0a0a0a;
      border-radius: 8px;
      transition: background-color 0.3s ease;
      margin-top: 10px;
    }

    button:hover {
      background-color: #ff00ff;
      color: #fff;
    }

    .discord-button {
      background-color: #7289DA; /* Discord blue */
      border: none;
      padding: 15px 30px;
      font-size: 1.2em;
      cursor: pointer;
      color: white;
      border-radius: 8px;
      transition: background-color 0.3s ease;
      margin-top: 10px;
    }

    .discord-button:hover {
      background-color: #5b6e96;
    }

    .hidden {
      display: none;
      margin-top: 50px;
      text-align: left;
    }

    #about {
      max-width: 800px;
      margin: 0 auto;
    }

    h2, h3 {
      color: #00ffff;
    }

    ul {
      text-align: left;
      margin: 20px 0;
      padding-left: 20px;
    }

    li {
      margin-bottom: 10px;
    }

    #announcement-section {
      background-color: #1e1e1e;
      padding: 20px;
      margin-top: 30px;
      border-radius: 8px;
    }

    #announcement-section h3 {
      color: #ff00ff;
    }

    #announcement-section ul {
      list-style-type: none;
      padding-left: 0;
    }

    #announcement-section ul li {
      background-color: #333333;
      padding: 10px;
      margin: 5px 0;
      border-radius: 8px;
    }

    #announcement-form input, #announcement-form textarea {
      width: 80%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 8px;
      border: none;
    }

    #announcement-form button {
      background-color: #ff00ff;
      color: white;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 8px;
    }

    #admin-password {
      width: 80%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 8px;
      border: none;
    }

  </style>
</head>
<body>
  <img src="https://media.discordapp.net/attachments/1365681695218466889/1365977300469944360/rumFZRb.png?ex=680fedbf&is=680e9c3f&hm=907a81c11475b4ad1954a1fc4c5d6d7587e34ed0ccd010da830161b0c564d488&=&width=405&height=405" alt="FLAK Logo" id="flak-logo">

  <div class="home">
    <h1>WELCOME TO FLAK</h1>
    <!-- Button for About Us -->
    <button onclick="showAbout()">About Us</button>
    <!-- Button for Join the Server (Discord) -->
    <a href="https://discord.gg/rVU4H7mcwF" target="_blank">
      <button class="discord-button">Join the Server</button>
    </a>
  </div>

  <div id="about" class="hidden">
    <h2>Welcome to FLAK!</h2>
    <p>We’re thrilled to have you join us! FLAK is more than just a server – it’s a community built for everyone who loves gaming, connecting, and exploring new interests together. Here, we celebrate our members’ unique passions, whether it’s diving into an intense game, chilling with friends, or getting focused in a study session.</p>

    <h3>💬 Chat Category</h3>
    <ul>
      <li>Hang out in General Chat for daily convos and random talks.</li>
      <li>Dive into Gaming Chat to team up, share tips, or flex your wins.</li>
      <li>Flex your gains or share fitness tips in Gym Chat.</li>
      <li>Rev your engines in Car Chat — show off your rides, discuss mods, share car news, and everything automotive</li>
      <li>Drop your best shots in Pics Chat — selfies, photography, artwork, anything visual.</li>
      <li>Post the funniest content in our Memes Chat — because who doesn’t love a good meme?</li>
      <li>Leveling system: the more you chat, the more perks you unlock!</li>
    </ul>

    <h3>🗣️ Talking Category</h3>
    <ul>
      <li>Create your own custom VC whenever you want.</li>
      <li>Personalize your hangout, bring your friends, vibe your way.</li>
    </ul>

    <h3>🎬 Movies Category</h3>
    <ul>
      <li>Watching Together Stage for movie watch-alongs.</li>
      <li>Two VC Channels for movie discussions.</li>
      <li>Movie & Show Suggestions Forum.</li>
    </ul>

    <h3>📚 Studying Category</h3>
    <ul>
      <li>Two Classroom Stages for study sessions and workshops.</li>
      <li>Two Students’ Lounges (VCs) for casual studying.</li>
      <li>Study-Topics Forum for sharing tips and organizing group studies.</li>
    </ul>

    <h3>🎥 Streaming Category</h3>
    <ul>
      <li>Live Stage for recordings and streams.</li>
      <li>Two VC Channels for gaming parties and live editing.</li>
      <li>Stream & Content Suggestions Forum.</li>
    </ul>

    <p>At FLAK, we’re not just here to build a server — we’re building a place where friendships form, passions grow, and good memories are made.
    We’re proud of the space we’ve created together, and we’re even more excited about where we’re headed next.</p>
  </div>

  <!-- Announcement Section -->
  <div id="announcement-section">
    <h3>Latest Announcements</h3>
    <ul id="announcement-list">
      <!-- Announcements will appear here -->
    </ul>

    <div id="announcement-form">
      <h4>Post a New Announcement</h4>
      <!-- Admin Password Input -->
      <input type="password" id="admin-password" placeholder="Enter Admin Password" />
      <input type="text" id="announcement-title" placeholder="Enter announcement title" />
      <textarea id="announcement-message" rows="4" placeholder="Enter announcement message"></textarea>
      <button onclick="postAnnouncement()">Post Announcement</button>
    </div>
  </div>

  <script>
    // Define the admin password
    const adminPassword = 'maatoq1'; // Replace with your desired password

    function showAbout() {
      document.getElementById('about').classList.toggle('hidden');
    }

    function postAnnouncement() {
      var title = document.getElementById('announcement-title').value;
      var message = document.getElementById('announcement-message').value;
      var password = document.getElementById('admin-password').value;

      // Check if the entered password matches the admin password
      if (password !== adminPassword) {
        alert("Invalid password. Only the admin can post announcements.");
        return;
      }

      // Check if both title and message are provided
      if (title && message) {
        var announcementList = document.getElementById('announcement-list');
        var newAnnouncement = document.createElement('li');
        newAnnouncement.innerHTML = `<strong>${title}</strong><p>${message}</p>`;
        announcementList.appendChild(newAnnouncement);

        // Clear the input fields after posting
        document.getElementById('announcement-title').value = '';
        document.getElementById('announcement-message').value = '';
        document.getElementById('admin-password').value = ''; // Clear the password field
      } else {
        alert("Please fill in both fields.");
      }
    }
  </script>
</body>
</html>
