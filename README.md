This is a minimal example of a VUE app which makes a call to the wikipedia Action API.

You should be able to get up and running by
[installing Node.js and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm),
cloning this repository, then from the top level directory, run ```npm run dev``` and navigate to ```http://localhost:5173/``` in your favorite browser.  You should see a "Userinfo!" button.  Click it and you should get some information about you as an unauthenticated user.

This code out as the demo app you get by running ```create-vue``` as described on the [Vue Quick Start Page](https://vuejs.org/guide/quick-start.html).  That was certainly a fast way to get a demo up and running, but I found it wasn't so great for me.  If you already know javascript (which I kind of do, but only barely) and you've used some of the other JS app frameworks, my guess is the demo app you get from ```create-view``` makes a lot of sense.  For me, however, it left me groping to understand how all the pieces fit together, and being totally perplexed how you could start making API calls against wikipedia and doc something useful.  It took me a few false starts and failed experiments to get to the point where I could make a single GET call and display the result.  Once I got there, I started hacking away everything that ```create-vue``` generated which wasn't necessary.  What's left is the code you see here.  I can't promise this is the best way to do things, but at least it's fairly minimal and demonstrates what to me was the key bit of functionality: making Action API calls.

I suspect the VUE documentation is very good for somebody who already knows Angular, React, or some other JS framework and is looking to pick up Vue.  The problem for me was that basically from step 1, you need to be making decisions.  Do I want Options or Composition?  Which flavor of export should I be using?  Do I want ```<script>``` or ```<script setup>```?  Do I want jquery or the new fetch() API?  Which of several possible styles of handing async calls do I want?  Do I want a single-page app, or to enhance an existing HTML page?  Do I want Single-File Components?  None of these are earth-shattering decisions by themselves, but they all add up to a lot of ways to make the wrong choices.  It also means a lot of the examples you find will be using a different style from the example you're looking at; somebody who's already a javascript expert will often be able to transpose on sight, but for me all I knew was it wasn' working.

Anyway, here's what I came up with.  I hope it's useful to somebody.
