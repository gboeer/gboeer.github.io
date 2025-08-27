---
layout: page
title: Which day is today?
tags: [Anniversaries, History, Events, Personal, On-This-Day]
permalink: /today/
---
<p>A collection of personally curated dates and events that caught my attention. This is not a comprehensive list of historical events, just my own selection of moments in time that reflect my own interests. For complete historical records, visit Wikipedia's "On this day" pages.</p>

<script>
function getTodayWikipediaLink() {
    const today = new Date();
    const monthNames = ["January", "February", "March", "April", "May", "June",
        "July", "August", "September", "October", "November", "December"];
    const month = monthNames[today.getMonth()];
    const day = today.getDate();
    return `https://en.wikipedia.org/wiki/${month}_${day}`;
}

document.addEventListener('DOMContentLoaded', function() {
    const link = document.getElementById('today-wikipedia-link');
    if (link) {
        link.href = getTodayWikipediaLink();
    }
});
</script>

<p style="text-align: center; margin: 20px 0;">
    <a id="today-wikipedia-link" href="#" target="_blank" style="font-weight: bold; color: #0066cc;">
        📅 View today's events on Wikipedia
    </a>
</p>

<button onclick="expandAllDetails(true)">Expand all</button>
<button onclick="expandAllDetails(false)">Collapse all</button>

<script>
function expandAllDetails(open) {
  document.querySelectorAll('details').forEach(d => d.open = open);
}
</script>

<details>
    <summary><strong>August 27, 2025 :: 🎉✨</strong></summary>
    <p>
        Today is Just Because Day!
        <br><br>
        It invites you to do something just because, without any particular reason.
    </p>
</details>

<details>
    <summary><strong>August 26, 2025 :: 🚀🇩🇪</strong></summary>
    <p>
        Today marks 47 years since the Soyuz 31 mission launched into space, carrying <a href="https://en.wikipedia.org/wiki/Sigmund_J%C3%A4hn" target="_blank">Sigmund Jähn</a>, the first German in space.
    </p>
</details>

<details>
    <summary><strong>August 25, 2025 :: 🐧💻 </strong></summary>
    <p>
        Today marks 34 years since <a href="https://en.wikipedia.org/wiki/Linus_Torvalds" target="_blank">Linus Torvalds</a> first announced that he was working on an open source operating system.
    </p>
</details>

<details>
    <summary><strong>August 22, 2025 :: 🎸🎭</strong></summary>
    <p>
        Today <a href="https://en.wikipedia.org/wiki/John_Lee_Hooker" target="_blank">John Lee Hooker</a> would have turned 108 years old.
        <br><br>
        It is also the death anniversary of <a href="https://en.wikipedia.org/wiki/Loriot" target="_blank">Loriot (Vicco von Bülow)</a>.

    </p>
</details>

<details>
    <summary><strong>August 20, 2025 :: 👾🎤</strong></summary>
    <p>
        Today <a href="https://en.wikipedia.org/wiki/H._P._Lovecraft" target="_blank">H.P. Lovecraft</a> would have turned 135 years old, and <a href="https://en.wikipedia.org/wiki/Rio_Reiser" target="_blank">Rio Reiser</a>, lead singer of the german band <a href="https://en.wikipedia.org/wiki/Ton_Steine_Scherben" target="_blank">"Ton Steine Scherben"</a> died 29 years ago.
    </p>
</details>

<details>
    <summary><strong>July 16, 2025 :: ☢️💥</strong></summary>
    <p>
        Today marks exactly 80 years since the first atomic bomb was detonated.
        <br><br>
        <a href="https://en.wikipedia.org/wiki/Trinity_(nuclear_test)" target="_blank">Learn more about the Trinity Test</a>
    </p>
</details>

<details>
    <summary><strong>July 4, 2025 :: 🎨🌲</strong></summary>
    <p>
        "There are no mistakes, just happy accidents."
        <br><br>
        Today marks 30 years since <a href="https://en.wikipedia.org/wiki/Bob_Ross" target="_blank">Bob Ross</a> passed away. Countless nights as a teenager, I lay in front of the TV and let him accompany me to sleep. Rest in Power.
    </p>
</details>

<button onclick="expandAllDetails(true)">Expand all</button>
<button onclick="expandAllDetails(false)">Collapse all</button>
