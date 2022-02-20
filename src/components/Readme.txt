

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