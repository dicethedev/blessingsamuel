

passing props to line of codes

{{content}}

then jump into is this line add this =====


    <button @click="selectTab(row.id)" v-for="row in content" class="work-places">
      <h1>{{row.title}}</h1>
    </button>

    jump to this and add this ===================

    <div v-if="currentTab == row.id" class="container">
      <h2>
        <span>{{row.title}}</span> --- Intern Software Engineer @
        <a href="https://www.printrite.ng" target="_blank" rel="noreferrer"
          >PrintriteNg
        </a>
      </h2>
      <h3>May 2021 - Present</h3>
      <ul>
        <li>Did my internship program at Printrite Ng.</li>
        <li>
          Work with languagues , platforms , frameworks, and content management
          systems such as PHP, VueJs, Github, Bitbucket, JavaScript, SQL and
          Figma.
        </li>
        <li>
          Communicate with integrative teams of developers, engineers, designers
          and clients.
        </li>
      </ul>
    </div>



      <!-- First Container -->
    <!-- Added a v-if directive here -->
    <div v-for="info in content" v-if="currentTab == 1" class="container">
      <h2>
        <span>{{ info.title }}</span> --- Intern Software Engineer @
        <a href="https://www.printrite.ng" target="_blank" rel="noreferrer"
          >PrintriteNg
        </a>
      </h2>
      <h3>May 2021 - Present</h3>
      <ul>
        <li>Did my internship program at Printrite Ng.</li>
        <li>
          Work with languagues , platforms , frameworks, and content management
          systems such as PHP, VueJs, Github, Bitbucket, JavaScript, SQL and
          Figma.
        </li>
        <li>
          Communicate with integrative teams of developers, engineers, designers
          and clients.
        </li>
      </ul>
    </div>


    Navigation display codes
         <ul v-show="!mobile" class="navigation">
        <li>
          <router-link class="nav-link" :to="{ name: '' }"
            ><span>01.</span>About</router-link
          >
        </li>

        <li>
          <router-link class="nav-link" :to="{ name: '' }"
            ><span>02.</span>Experience</router-link
          >
        </li>

        <li>
          <router-link class="nav-link" :to="{ name: '' }"
            ><span>03.</span>Work</router-link
          >
        </li>

        <li>
          <router-link class="nav-link" :to="{ name: '' }"
            ><span>04.</span>Contact</router-link
          >
        </li>

        <!-- Resume Button area is here -->
        <!-- href="/resume.pdf" -->
        <a class="resume-button" href="#" target="_blank">Resume</a>
      </ul>

      <!-- Nav Bar Icon when you switch to mobile -->
      <!-- Toogle Mobile Nav is click event for opening nav closing when you switch to mobile -->
      <!-- the icon-active is displaying when the mobileNav is true and the mobileNav will be trigger by toggleMobileNav -->
      <div class="icon">
        <img
          @click="toggleMobileNav"
          v-show="mobile"
          src="@/assets/Nav-bar.svg"
          :class="{ 'icon-active': mobileNav }"
        />
      </div>

      <!-- Animating the mobileNav here -->
      <!-- v-show id mobileNav is true here -->

      <transition name="mobileNav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <!-- The Nav-close-bar and binded property is in this image area -->
          <img
            @click="toggleMobileNav"
            v-show="mobile"
            class="nav-close-bar"
            src="@/assets/Nav-close-bar.svg"
            :class="{ 'icon-active-2': mobileNav }"
          />

          <li>
            <a
              class="nav-link button_style_focus"
              href="/#about"
              :to="{ name: '' }"
              ><span>01.</span>About</a
            >
          </li>

          <li>
            <a
              class="nav-link button_style"
              href="/#experience"
              :to="{ name: '' }"
              ><span>02.</span>Experience</a
            >
          </li>

          <li>
            <a class="nav-link button_style" href="/#works" :to="{ name: '' }"
              ><span>03.</span>Work</a
            >
          </li>

          <li>
            <a class="nav-link button_style" href="/#contact" :to="{ name: '' }"
              ><span>04.</span>Contact</a
            >
          </li>
          <!-- Resume Button area is here -->
          <!-- href="/resume.pdf" -->
          <a class="resume-link" href="#" target="_blank" rel="">Resume</a>
        </ul>
      </transition>

      <style>
      
    // The navigation is the class the name for all the nav link
    .navigation {
      display: flex;
      padding: 12px 0;
      justify-content: flex-end;
      align-items: center;
      margin-left: 32.0625rem;
    }

    
    ul,
    .nav-link {
      font-weight: 400;
      color: var(--slate);
      list-style: none;
      text-decoration: none;
    }

    // The nav listing style here
    li {
      padding: 10px;
      margin-left: 10px;
    }

    .nav-link span {
      color: #00cffd;
      font-style: normal;
      font-weight: normal;
      //13px = 0.8125rem
      font-size: 0.875rem;
      margin-right: 0.325rem;
    }

    .nav-link {
      //17px = 1.0625rem
      font-size: 1rem;
      transition: var(--transition);
      padding-bottom: 4px;
      margin-right: 1.1625rem;

      &:hover {
        border: 1px dashed #00cffd;
        padding: 12px;
        border-radius: 0.625rem;
      }

      
    // Nav-bar styling is here
    .icon {
      display: flex;
      align-items: center;
      position: absolute;
      top: 0;
      right: 24px;
      height: 100%;

      // Nav-bar hamburger styling is here
      img {
        top: 2.4375rem;
        cursor: pointer;
        //45px & 35px
        width: 2.8125rem;
        height: 2.1875rem;
        transition: 0.8s ease all;

        &:hover {
          border: 1px dashed #00cffd;
          padding: 9px;
          //10px = 0.625rem
          border-radius: 0.625rem;
        }
      }
    }

    // Nav-bar animating to rotate to Nav-close-bar
    .icon-active {
      transform: rotateX(180deg);
      transition: 300ms ease-in-out;
    }

    // The dropdown menu when you click on Nav-bar on mobile
    .dropdown-nav {
      position: fixed;
      display: flex;
      justify-content: center;
      flex-direction: column;
      width: 100vw;
      height: 100%;
      right: 0;
      margin: 0;
      outline: 0;
      max-width: 21.1875rem;
      background-color: #16294b;
      transform: translate(0vw);
      transition: 200ms ease-in-out;

      // Nav-close-bar hamburger styling is here
      img {
        position: absolute;
        cursor: pointer;
        top: 1.5rem;
        margin-left: 17.1875rem;
        margin-right: 3rem;
        //45px & 35px
        width: 2.8125rem;
        height: 2.1875rem;
        // padding-top: -5%;
        transition: 200ms ease-in-out;

        &:hover {
          border: 1px dashed #00cffd;
          padding: 6px;
          //10px = 0.625rem
          border-radius: 0.625rem;
        }
      }

      li {
        .nav-link {
          position: relative;
          display: flex;
          justify-content: center;
          align-items: center;
          text-decoration: none;
          color: #fff;
          //18px = 1.125rem
          font-size: 1.125rem;
          font-weight: 400;
        }

        .nav-link {
          //117px = 7.1875rem
          margin-left: 3.1875rem;
        }

        span {
          //16px // 10px = 0.625rem
          font-size: 1rem;
          font-weight: 400;
          color: #112240;
        }
      }

      .button_style_focus {
        background: linear-gradient(
          89.92deg,
          #00cffd 8.68%,
          rgba(0, 233, 223, 0.2) 73.43%
        );
        border-radius: 40px 0px 0px 10px;
        width: 16.875rem;
        height: 3.125rem;
      }

      .button_style {
        background: linear-gradient(
          89.92deg,
          rgba(0, 207, 253, 0.31) 8.68%,
          rgba(0, 233, 223, 0.22) 73.43%
        );
        border-radius: 40px 0px 0px 10px;
        width: 16.875rem;
        height: 3.125rem;
        outline: none;

        &:hover {
          background: linear-gradient(
            89.92deg,
            #00cffd 8.68%,
            rgba(0, 233, 223, 0.2) 73.43%
          );
          transform: translateY(-7px);
          transition: 300ms ease-in-out;
        }
        &:active {
          transform: translateY(-1px);
        }
      }
    }

    .resume-link {
      cursor: pointer;
      margin-left: 6.1875rem;
      margin-right: 5.125rem;
      //80px = 5rem
      margin-top: 5rem;
      color: #00cffd;
      background-color: transparent;
      font-size: 16px;
      width: max-content;
      border: 1px solid #00cffd;
      border-radius: 0.625rem;
      line-height: 1;
      //10px = 0.625rem
      padding: 1.125rem 3.125rem;
      text-decoration: none;
      transition: var(--transition);

      &:hover {
        color: #fff;
        background-color: rgba(13, 186, 255, 0.185);
        transition: transform 100ms var(--transition);
      }
    }
      
      </style>
