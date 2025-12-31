<script>
  import emblaCarouselVue from 'embla-carousel-vue'
  import Autoplay from 'embla-carousel-autoplay'
  
  
  export default {
    
    setup() {
       
        const autoplayOptions = {
        delay: 2000,
        rootNode: (emblaRoot) => emblaRoot.parentElement
        }

      const [emblaNode] = emblaCarouselVue({ loop: true }, [Autoplay(autoplayOptions)])
      return { emblaNode }
    },
  }
</script>
<template>
    <main>
        <div class="mainimg">
            <img src="/assets/gwhmun_logo.png" class="commlogo">
            <h1 class="title">GWH JMUN 2025</h1>
            <h2 class="subtitle">For grades 6-8 only</h2>
            <h2 class="subtitle">16th & 17th January</h2>
        </div>
        
        <h1 class="msg-title">Flow of Events</h1>
        <div class="flow">
            <div class="day">
                <h1>Day 1</h1>
                <p>Reporting time to school: 7:45 AM</p>
                <p>Registrations: 7:45 - 8:30 AM</p>
                <p>Opening Ceremony: 8:45 - 9:15 AM</p>
                <p>Juice Break: 9:15 - 9:30 AM</p>
                <p>Committee Session 1: 9:30 AM - 12:20 PM</p>
                <p>Lunch: 12:20 - 1:00 PM</p>
                <p>Committee Session 2: 1:00 PM - 2:00 PM</p>
                <p>Disperal: 2:00PM</p>
            </div>
            <div class="day">
                <h1>Day 2</h1>
                <p>Reporting time to school (at the respective committee rooms): 7:45 AM</p>
                <p>Committee Session 3: 8:00 - 10:00 AM</p>
                <p>Break: 10:00 - 10:15 AM</p>
                <p>Committee Session 4: 10:15 AM - 12:15 PM</p>
                <p>Lunch: 12:15 - 12:50 PM</p>
                <p>Closing Ceremony: 1:00 - 2:00 PM</p>
                <p>Dispersal: 2:00 PM</p>
                
            </div>
        </div>
        <h2  style="text-align:center; font-weight: 3000;">Device Policy: </h2>
        <h4  style="text-align:center;">All delegates are permitted to bring their laptops.</h4>
        <h4  style="text-align:center;">Mobile phones can only be brought by external students.</h4>
        <h4  style="text-align:center;">They must be kept switched off and not used on school premises.</h4>
        <h1 class="msg-title">Letter from the Secretary General</h1>
        
        <div class="msg">
            <div class="info">
                <img src="/assets/eb_pics/DISEC/Amisha Sharma.jpg">
                <h2 class="name">Amisha Sharma</h2>
                <h3 class="tl">Secretary General</h3>
            </div>
            <div class="desc">{{`Dear Delegates, 

It’s a true honor to address all of you as the Secretary General of the GWHJMUN 2025. It’s a joy to see so many of you attending your first ever Model UN conference, on the brink of embarking on this journey of becoming more aware, responsible global citizens. 

When you enter your committee sessions, delegates, do not think of how little you know, and try to put your overwhelming desire for the Best Delegate award out of your mind for a moment. As you enter, simply cherish this wonderful opportunity you’ve been given: you get to start your Model UN career. Over the course of the 20 MUNs I’ve been to personally, I’ve seen myself transform from a tiny 14 year old, shaking as she entered the UNCSW, barely able to give a single GSL, into standing here in front of you today. I’m confident that each and every one of you is going to find bravery and courage you never thought you had, going in front of your committees to deliver amazing speeches. Even if you don’t think you have that bravery, go give the speech anyway. I promise, you’ll find that you had it all along. The beauty of this being your first time is that there is nothing to compare yourself to: every single action you take is a victory. Make a friendship with a delegate from another school. Help write a clause of the resolution. Ask a POI even if you’re not quite sure you’re phrasing it right. Do not let the fear of failing hold you back - nobody cares if you fall today, as long as you get back up tomorrow. 

As the first ever inter school JMUN Greenwood High has hosted, I would like to warmly welcome every external delegate in the room. I applaud you all, for stepping out of your comfort zone, and putting in the effort to be here today. A final word of advice for you all: the loudest voice in the room is very rarely the smartest, or the most qualified. Do not be a power delegate, and don’t let the fact that you’re currently shouting over everyone else trick you into thinking you’re a good leader. A good leader doesn’t have to be smart, or qualified, and they certainly don’t need to be loud. They need to be kind, above anything. They need to involve other people in the discussions, create opportunities for collaboration, and have a singular goal: to help the world become a better place. So as you go off into the world of MUN, though sometimes you will feel like you have to be cutthroat and clever, and sometimes yes, you will have to be, I will leave you with a quote most of you are probably familiar with already: if you can be anything in the world, be kind. 

All the very best, 
Amisha Sharma
`}}</div>
        </div>
        <!--
        <h1 class="msg-title">Letter from the Director General</h1>
        <div class="msg">
          <div class="info">
                <img src="/assets/eb_pics/IPC/Aarush Vyas.png">
                <h2 class="name">Aarush Vyas</h2>
                <h3 class="tl">Director General</h3>
            </div>
            <div class="desc">{{`“I would rather have questions that can’t be answered rather than answers that can’t be questioned.” - Richard Feynmann.\n\nHumanity’s progress came through curiosity. If an early human didn’t stumble out of their cave to investigate the blinding, orange plume that lit up a tree in front of them, humanity would have never harnessed fire. If we never thought to make things more efficient, we never would have invented the wheel or the carriage. Humanity’s ability to inquire, think, and act accordingly has brought it from apehood to the world’s de facto apex predator.\n\nAs humans, there is no ceiling too high to reach, and no limit to how quickly we can do it.\n\nAs young thinkers and our world’s future, you must steer humanity back onto the right path, and seeing as we will soon get our hands on the reins, this generation and those to come must be prepared.\n\nGeopolitics in this era of tomorrow’s history seem like a storm; thundering, crashing, frightening. It may seem like a fool’s errand to fight the weather, but geopolitical disasters are not forces of nature and are most certainly not impossible to steer away. Everything you see in the news is a consequence of a decision made by a human. \n\nOur job as humans is to ensure that our comrades’ actions result in headlines of jubilation, rather than dread, and there is no better way to understand that than to get down in the mud with the crises and the cover-ups, to see what makes the world tick. There are no heroes in this story, nor are there villains. There are people, their visions, and their will to take action.\n\nWelcome to Greenwood High’s Junior Model United Nations 2024. \n\nIn the coming days, you will have to navigate the high seas of diplomacy, tiptoe down the creaky stairs of international law, and be a little shady. Research, investigate, and fight tooth and nail. You are not the spectators, but the protagonists. Seize the moment, and make it yours.\n\nBe the change you want to see by making the changes you want to see. The only thing that you need to change the world is a desire to do so, and the will to make it happen.\n\nSincerely,\nAarush Vyas\nDirector General`}}</div>   
        </div>
        -->
    </main>
    <div class="embla" ref="emblaNode">
      <div class="embla__container">
        <div class="embla__slide"><img src="/assets/carousel/File_1.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_2.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_3.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_4.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_6.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_7.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_8.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_9.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_10.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_11.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_12.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_13.jpg " width="600rem"  height="400rem" ></div>
        <div class="embla__slide"><img src="/assets/carousel/File_14.jpg " width="600rem"  height="400rem" ></div>
      </div>
    </div>
</template>

<style scoped>
main {
    padding: 10px;
}

.mainimg {
    margin: 0 10px;
    border: 2px solid #3b3b3b;
    border-radius: 20px;
    padding: 125px 15px;
    display: flex;
    flex-direction: column;
    text-align: center;
    background-image: url('/assets/mainimg.png');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    align-items: center;
}

h1.title {
    font-size: 3.5em;
    margin: 5px;
}

h2.subtitle {
    font-weight: normal;
    font-size: 1.75em;
    margin: 5px
}

.commlogo {
    width: 300px;
}

.embla {
    overflow: hidden;
  }
  .embla__container {
    display: flex;
    margin: auto;
    width: 50%;
    padding: 10px;
  }
  .embla__slide {
    flex: 0 0 100%;
    min-width: 0;
  }

  .msg {
    display: flex;
    align-items: center;
    margin: 15px 5%;
    padding-bottom: 1em;
    border-bottom: 1px solid #363636;
    text-align: center;
}

.info {
    padding: 0 5%;
    text-align: center;
}

.info > img {
    border: 1px solid #363636;
    border-radius: 50%;
}

@media(min-width: 800px) {
    .msg {
        flex-direction: row;
        justify-content: space-between;
    }   
    .desc {
        width: 80%;
    }
    .info {
        width: 30%
    }
    .info > img {      
        width: 80%;
    }
}

@media(max-width: 800px) {
    .msg {
        flex-direction: column;
    }
    .desc {
        width: 100%;
    }
    .info {
        width: 100%
    }
    .info > img {
        width: 60%;
    }
}

.desc {
    padding: 5px 0;
    white-space: pre-wrap;
}

h2.name {
    font-size: 1.75em;
    margin: 0;
}

h3.tl {
    font-size: 1.25em;
    margin: 0;
    font-weight: normal;
}

h1.msg-title {
    text-align: center;
    font-size: 2.5em;
}

.flow {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    margin-top: 50px;
    flex-wrap: wrap;
}

.day {
    border: 1px solid #363636;
    border-radius: 20px;
    padding: 50px 15px;
    text-align: center;
    width: 40%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.day p {
    margin: 5px;
    font-size: 1.1em;
}
</style>
