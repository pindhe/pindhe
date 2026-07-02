<svg width="100%" height="320" viewBox="0 0 900 320" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#050810"/>
      <stop offset="45%" stop-color="#0b1024"/>
      <stop offset="100%" stop-color="#150a2e"/>
    </linearGradient>

    <linearGradient id="textGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#22d3ee"/>
      <stop offset="50%" stop-color="#a78bfa"/>
      <stop offset="100%" stop-color="#facc15"/>
    </linearGradient>

    <linearGradient id="subGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#67e8f9"/>
      <stop offset="100%" stop-color="#c4b5fd"/>
    </linearGradient>

    <filter id="glow" x="-60%" y="-60%" width="220%" height="220%">
      <feGaussianBlur stdDeviation="7" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="softGlow" x="-60%" y="-60%" width="220%" height="220%">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <radialGradient id="orbGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#67e8f9" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#67e8f9" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="orbGlow2" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#facc15" stop-opacity="0.45"/>
      <stop offset="100%" stop-color="#facc15" stop-opacity="0"/>
    </radialGradient>

    <clipPath id="frameClip">
      <rect x="0" y="0" width="900" height="320" rx="18"/>
    </clipPath>
  </defs>

  <g clip-path="url(#frameClip)">
    <rect width="900" height="320" fill="url(#bgGrad)"/>

    <!-- ambient glow orbs -->
    <circle cx="120" cy="60" r="140" fill="url(#orbGlow)">
      <animate attributeName="opacity" values="0.5;0.9;0.5" dur="4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="800" cy="270" r="160" fill="url(#orbGlow2)">
      <animate attributeName="opacity" values="0.4;0.8;0.4" dur="5s" repeatCount="indefinite"/>
    </circle>

    <!-- starfield -->
    <g fill="#ffffff">
      <circle cx="60" cy="40" r="1.4" opacity="0.7"><animate attributeName="opacity" values="0.2;1;0.2" dur="3s" repeatCount="indefinite"/></circle>
      <circle cx="820" cy="35" r="1.6" opacity="0.6"><animate attributeName="opacity" values="0.1;0.9;0.1" dur="2.6s" repeatCount="indefinite"/></circle>
      <circle cx="760" cy="90" r="1.2" opacity="0.5"><animate attributeName="opacity" values="0.2;0.8;0.2" dur="3.4s" repeatCount="indefinite"/></circle>
      <circle cx="50" cy="260" r="1.5" opacity="0.6"><animate attributeName="opacity" values="0.1;0.9;0.1" dur="2.9s" repeatCount="indefinite"/></circle>
      <circle cx="870" cy="230" r="1.3" opacity="0.5"><animate attributeName="opacity" values="0.2;0.8;0.2" dur="3.7s" repeatCount="indefinite"/></circle>
      <circle cx="450" cy="20" r="1.1" opacity="0.5"><animate attributeName="opacity" values="0.1;0.7;0.1" dur="3.1s" repeatCount="indefinite"/></circle>
    </g>

    <!-- rotating 3D-ish tech ring behind text -->
    <g transform="translate(450,150)">
      <ellipse cx="0" cy="0" rx="330" ry="60" fill="none" stroke="#22d3ee" stroke-opacity="0.18" stroke-width="1.5">
        <animateTransform attributeName="transform" type="rotate" from="0 0 0" to="360 0 0" dur="18s" repeatCount="indefinite"/>
      </ellipse>
      <ellipse cx="0" cy="0" rx="280" ry="100" fill="none" stroke="#a78bfa" stroke-opacity="0.14" stroke-width="1.2">
        <animateTransform attributeName="transform" type="rotate" from="360 0 0" to="0 0 0" dur="24s" repeatCount="indefinite"/>
      </ellipse>
    </g>

    <!-- floating code brackets, subtle wobble -->
    <text x="70" y="120" font-family="Consolas, 'Courier New', monospace" font-weight="700" font-size="46" fill="#22d3ee" fill-opacity="0.35">
      &lt;/&gt;
      <animate attributeName="y" values="120;110;120" dur="3.5s" repeatCount="indefinite"/>
    </text>

    <text x="790" y="250" font-family="Consolas, 'Courier New', monospace" font-weight="700" font-size="40" fill="#facc15" fill-opacity="0.3">
      { AI }
      <animate attributeName="y" values="250;262;250" dur="4s" repeatCount="indefinite"/>
    </text>

    <!-- main name -->
    <text x="450" y="148" text-anchor="middle" font-family="Segoe UI, Arial, sans-serif" font-weight="800" font-size="58" fill="url(#textGrad)" filter="url(#glow)">
      Nour Hassan Pindhe
      <animate attributeName="opacity" values="0.75;1;0.75" dur="3s" repeatCount="indefinite"/>
    </text>

    <!-- subtitle -->
    <text x="450" y="192" text-anchor="middle" font-family="Segoe UI, Arial, sans-serif" font-weight="600" font-size="22" letter-spacing="1" fill="url(#subGrad)" filter="url(#softGlow)">
      Full-Stack Developer • UI/UX Designer • AI Engineer
    </text>

    <!-- tagline pill -->
    <g transform="translate(450,236)">
      <rect x="-190" y="-18" width="380" height="36" rx="18" fill="#0f172a" stroke="#22d3ee" stroke-opacity="0.5"/>
      <text x="0" y="6" text-anchor="middle" font-family="Consolas, 'Courier New', monospace" font-size="15" fill="#67e8f9">
        🤖 Building AI-Powered Solutions from Hargeisa, Somaliland
      </text>
    </g>

    <!-- bottom scan line glow -->
    <rect x="0" y="308" width="900" height="2" fill="url(#textGrad)" opacity="0.6">
      <animate attributeName="opacity" values="0.3;0.8;0.3" dur="2.5s" repeatCount="indefinite"/>
    </rect>
  </g>

  <rect x="1" y="1" width="898" height="318" rx="18" fill="none" stroke="url(#textGrad)" stroke-opacity="0.4" stroke-width="1.5"/>
</svg>

<h1 align="center">Hi 👋, I'm Nour hassan pindhe</h1>
<h3 align="center">FULL STACK & Artificial Intelligence</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=pindhe&label=Profile%20views&color=0e75b6&style=flat" alt="pindhe" /> </p>

<p align="left"> <a href="https://github.com/ryo-ma/github-profile-trophy"><img src="https://github-profile-trophy.vercel.app/?username=pindhe" alt="pindhe" /></a> </p>

- 🌱 I’m currently learning **Courses**

- 📫 How to reach me **kharash420@gmail.com**

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://fb.com/https://www.facebook.com/pindhe2k" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/facebook.svg" alt="https://www.facebook.com/pindhe2k" height="30" width="40" /></a>
<a href="https://instagram.com/https://www.instagram.com/pindhe_1/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="https://www.instagram.com/pindhe_1/" height="30" width="40" /></a>
<a href="https://dribbble.com/https://dribbble.com/nor-pindhe" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/dribbble.svg" alt="https://dribbble.com/nor-pindhe" height="30" width="40" /></a>
<a href="https://www.youtube.com/c/https://www.youtube.com/@pindhe" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/youtube.svg" alt="https://www.youtube.com/@pindhe" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://developer.android.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original-wordmark.svg" alt="android" width="40" height="40"/> </a> <a href="https://www.blender.org/" target="_blank" rel="noreferrer"> <img src="https://download.blender.org/branding/community/blender_community_badge_white.svg" alt="blender" width="40" height="40"/> </a> <a href="https://getbootstrap.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg" alt="bootstrap" width="40" height="40"/> </a> <a href="https://www.w3schools.com/cs/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" alt="csharp" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.djangoproject.com/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/django.svg" alt="django" width="40" height="40"/> </a> <a href="https://www.figma.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/figma/figma-icon.svg" alt="figma" width="40" height="40"/> </a> <a href="https://flutter.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg" alt="flutter" width="40" height="40"/> </a> <a href="https://cloud.google.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" alt="gcp" width="40" height="40"/> </a> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://golang.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg" alt="go" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://gohugo.io/" target="_blank" rel="noreferrer"> <img src="https://api.iconify.design/logos-hugo.svg" alt="hugo" width="40" height="40"/> </a> <a href="https://www.java.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://kafka.apache.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/apache_kafka/apache_kafka-icon.svg" alt="kafka" width="40" height="40"/> </a> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://www.mongodb.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="mongodb" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://www.nginx.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nginx/nginx-original.svg" alt="nginx" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://www.oracle.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/oracle/oracle-original.svg" alt="oracle" width="40" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.photoshop.com/en" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg" alt="photoshop" width="40" height="40"/> </a> <a href="https://www.php.net" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="php" width="40" height="40"/> </a> <a href="https://www.postgresql.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://reactjs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> <a href="https://reactnative.dev/" target="_blank" rel="noreferrer"> <img src="https://reactnative.dev/img/header_logo.svg" alt="reactnative" width="40" height="40"/> </a> <a href="https://www.sqlite.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" alt="sqlite" width="40" height="40"/> </a> <a href="https://developer.apple.com/swift/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/swift/swift-original.svg" alt="swift" width="40" height="40"/> </a> <a href="https://tailwindcss.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" alt="tailwind" width="40" height="40"/> </a> <a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="typescript" width="40" height="40"/> </a> <a href="https://vuejs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original-wordmark.svg" alt="vuejs" width="40" height="40"/> </a> </p>

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=pindhe&show_icons=true&locale=en&layout=compact" alt="pindhe" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=pindhe&show_icons=true&locale=en" alt="pindhe" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=pindhe&" alt="pindhe" /></p>
