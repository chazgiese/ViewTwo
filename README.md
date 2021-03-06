ViewTwo (Tumblr Theme)
======
### Fully responsive Tumblr theme that shows only two post at a time
![alt tag](https://56.media.tumblr.com/4fbeecd0dd1b32097722af4f3adc1854/tumblr_o3jcvpyLzW1vnrzo2o1_1280.png)


How to Install
-----
####Download the [ViewTwo.html](https://github.com/chazgiese/ViewTwo/blob/master/ViewTwo.html) file and/or copy and paste the code below into the "Edit HTML" section of your tumblr. I recommend downloading the ViewTwo.html file because this way you ensure you're getting the most up to date version.

```html
<!DOCTYPE html>
<!--
  ____________
  View—————Two              viewtwo-theme
                                  .tumblr
                                     .com

  w/♥
  www.chazgie.se

-->

<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{Title}
      {block:PostSummery} | {PostSummery}{/block:PostSummery}
    </title>
    {block:Description}
      <meta name="description" content="{MetaDescription}" />
    {/block:Description}
    <link rel="shortcut icon" href="{Favicon}" />
    <script type="text/javascript" src="http://static tumblr.com/q0etgkr/EIBmz7s0p/infinitescrolling.js">
    </script>
    <link href='https://fonts.googleapis.com/css?family=Karla:400,700,400italic' rel='stylesheet' type='text/css'>
    <!--PERSONAL CONTROLS START-->
    <meta name="color:Background" content="#ffffff" />
    <meta name="color:Background Nav" content="#ffffff" />
    <meta name="color:Nav Text Color" content="#000000" />
    <meta name="color:Nav Text Hover Color" content="inherit" />
    <!-- <meta name="if:Controls On Index" content="0"/> -->
    <!--<meta name="font:PostCaption" content="'Karla'"/>-->
    <meta name="if:Archive Link" content="1"/>
    <meta name="if:Dashboard Link" content="0"/>
    <!-- <meta name="if:Caption" content="0"/> -->
    <meta name="if:Ask Link" content="0"/>
    <meta name="text:Link 1 Name" content=""/>
    <meta name="text:Link 1 URL" content=""/>
    <meta name="text:Link 2 Name" content=""/>
    <meta name="text:Link 2 URL" content=""/>
    <meta name="text:Link 3 Name" content=""/>
    <meta name="text:Link 3 URL" content=""/>
    <meta name="text:Link 4 Name" content=""/>
    <meta name="text:Link 4 URL" content=""/>
    <!--PERSONAL CONTROLS END-->
    <style type="text/css">
/****************************************** CSS STARTS */
    /*
    ___________________
          GLOBAL STYLES
          & RESETS
    */
    * {
      webkit-box-sizing: border-box;
      moz-box-sizing: border-box;
      box-sizing: border-box;
      overflow: visible;
    }
    html,
    body {
      width: 100%;
      margin: 0;
      padding: 0;
    }
    body {
      background: {color:Background};
    }
    iframe#tumblr_controls {
      display:none;
    }
    p {
      margin: 0;
      padding: 0;
    }
    a,
    a:visited,
    a:hover {
      color: inherit;
      text-decoration: none;
      font-weight: inherit;
    }
    .post-container,
    .post,
    nav,
    .tumblr-controls {
      display: -webkit-flex;
      display: flex;
      justify-content: center;
    }
    /*
    ________________
          TYPOGRAPHY
    */
    body {
      font-family: 'Karla';
      font-weight: normal;
      font-size: 1.22rem;
    }
    nav {
      font-family: 'Karla';
      font-size: 1.22rem;
      color: {color:Nav Text Color};
    }
    nav a:hover {
      color: {color:Nav Text Hover Color};
    }
    /*
    ________________
          NAVIGATION
    */
    header {
      position: fixed;
      width: 100%;
      max-width: 100%;
      background-image: linear-gradient(0deg,rgba(255,255,255,0.00) 0%,{color:Background Nav} 50%);
      z-index: 999;
    }
    nav {
      flex-direction: -webkit-row;
      flex-direction: row;
      align-items: flex-start;
      padding: 1rem;
    }
    nav a {
    }
    #nav-left,
    #nav-right {
      width: 30%;
    }
    #nav-left {
      margin-right: auto;
    }
    #nav-left a {
      padding-right: 0.66rem;
    }
    #nav-right {
      margin-left: auto;
      text-align: right;
    }
    #nav-right a {
      padding-left: 0.66rem;
    }

    #archive,
    #ask,
    #dashboard {
      display: none;
    }

    {block:IfDashboardLink}
    #dashboard {
      display: inline-block;
    }
    {/block:IfDashboardLink}

    {block:IfArchiveLink}
    #archive {
      display: inline-block;
    }
    {/block:IfArchiveLink}

    {block:IfAskLink}
    #ask {
      display: inline-block;
    }
    {/block:IfAskLink}

    #hi {
      position: fixed;
      bottom: 3rem;
      left: -0.888rem;
      font-size: 0.36rem;
      letter-spacing: 0.123rem;
      color: #eaeaea;
      transform: rotate(90deg);
    }
    #hi:hover {
      color: #666;
      text-shadow: 0 0 4px #fff;
    }
    /*
    _________________
          POST LAYOUT
    */
    img,
    .post-container {
      max-width: 100%;
    }
    .post-container,
    .post {
      flex-direction: -webkit-column;
      flex-direction: column;
      justify-content: center;
    }
    .post-container {
      margin: 0 auto;
      padding-top: 4rem;
    }
    .post {
      margin-bottom: 6.66rem;
      padding: 0.666rem;
      height: 100vh;
      text-align: center;
    }
    .post:last-child {
      margin-bottom: 0;
    }
    {block:IfCaption}
    .post a {
      margin-top: auto;
    }
    {/block:IfCaption}
    .post img {
      max-height: 69vh;
      padding: 0rem;
    }
    .post p {
      margin-top: auto;
      padding-bottom: 1.66rem;
      max-height: 1.66rem;
      overflow: hidden;
    }

    .photoset a {
      display: none;
    }
    .photoset a:first-child {
      display: inline-block;
    }
    .tumblr-controls {
      flex-direction: -webkit-row;
      flex-direction: row;
      justify-content: space-between;
    }

    /*
    ____________________
          TABLET/DESKTOP
          LAYOUT CHANGES
    */
    @media (max-height: 425px) and (orientation: landscape) {
      .post p {
        display: none;
      }
      .post a {
        margin-bottom: auto;
      }
    }
    @media screen and (min-width: 600px) {
      .post {
        flex-basis: 50%;
        max-width: 50%;
        height: 97vh;
        max-height: 97vh;
        padding: 1.33rem;
      }
      .post-container {
        padding: 3vh 3rem 0;
        flex-direction: -webkit-row;
        flex-direction: row;
        flex-wrap: -webkit-wrap;
        flex-wrap: wrap;
      }
    }
/********************************************* CSS END */
    </style>

  </head>

  <header><!--NAVIGATION START-->
    <nav>
      <div id="nav-left">
        <a href="/archive" id="archive">Archive</a>
        <a href="/ask" id="ask">Ask</a>
        {block:IfLink1URL}
        <a href="{text:Link 1 URL}">
          {text:Link 1 Name}
        </a>
        {/block:IfLink1URL}
        {block:IfLink2URL}
        <a href="{text:Link 2 URL}">
          {text:Link 2 Name}
        </a>
        {/block:IfLink2URL}
        {block:IfLink3URL}
        <a href="{text:Link 3 URL}">
          {text:Link 3 Name}
        </a>
        {/block:IfLink3URL}
        {block:IfLink4URL}
        <a href="{text:Link 4 URL}">
          {text:Link 4 Name}
        </a>
        {/block:IfLink4URL}
      </div>
      <div id="nav-center">
        <a href="/" id="title">{Title}</a>
      </div>
      <div id="nav-right">
        <a href="http://www.tumblr.com/" id="dashboard">Dashboard</a>
        <a href="http://www.tumblr.com/follow/{Name}">Follow</a>
      </div>
    </nav>
  </header><!--NAVIGATION END-->

  <body>
    <div class="post-container"><!--CONTAINS ALL POST CONTENT-->
    {block:Posts}<!--TUMBLR POST START-->

      {block:Photo}<!--PHOTO POST-->
      <div class="post photo">
        {block:PermalinkPage}
          <div class="tumblr-controls perma">
            {LikeButton color="black" size="18"}
            {ReblogButton color="black" size="18"}
          </div>
        {/block:PermalinkPage}
        <a href="{Permalink}">
          <img src="{PhotoURL-HighRes}" />
        </a>
        {block:IndexPage}
          {block:IfControlsOnIndex}
          <div class="tumblr-controls index">
            {LikeButton color="black" size="18"}
            {ReblogButton color="black" size="18"}
          </div>
          {/block:IfControlsOnIndex}
        {/block:IndexPage}

        {block:IfCaption}{block:Caption}{Caption}{/block:Caption}{/block:IfCaption}
      </div>
      {/block:Photo}<!--PHOTO POSTS END-->

      {block:Photoset}<!--PHOTOSET POSTS -->
      <div class="post photoset">
        	{Photoset}
        {block:IfCaption}{block:Caption}{Caption}{/block:Caption}{/block:IfCaption}
      </div>
      {/block:Photoset} <!--PHOTOSET POSTS END---->

      {block:Video}<!--VIDEO POSTS-->
      <div class="post video">
        {Video-300}
        {block:IfCaption}{block:Caption}{Caption}{/block:Caption}{/block:IfCaption}
      </div>
      {/block:Video}<!--VIDEO POSTS END-->

      {block:Audio}<!--AUDIO POSTS-->
      <div class="post audio">
        {AudioPlayerWhite}
        <br>{PlayCountWithLabel}<br>
        {block:IfCaption}{block:Caption}{Caption}{/block:Caption}{/block:IfCaption}
      </div>
      {/block:Audio}<!--AUDIO POSTS END-->

      {block:Quote}<!--QUOTE POSTS-->
      <div class="post quote">
        "{Quote}"
        {block:Source}<br>{Source}{/block:Source}
      </div>
      {/block:Quote}<!--QUOTE POSTS END-->

      {block:Text}<!--TEXT POSTS-->
      <div class="post text">
        {block:Title}
          {Title}
          <br>
        {/block:title}
        {body}
      </div>
      {/block:Text}<!--TEXT POSTS END-->

      {block:Answer}<!--ASK POSTS-->
      <div class="post ask">
        {Question}<br>
        {Asker}<br>
        {Answer}
      </di>
      {/block:Answer}<!--ASK POSTS END-->

      {block:Chat}<!--CHAT POSTS-->
      <div class="post chat">
        {block:Title}{Title}<br>{/block:Title}
        {block:Lines}
        {block:Label}<strong>{Label}</strong>{/block:Label} {Line}<br>
        {/block:Lines}
      </div>
      {/block:Chat}<!--CHAT POSTS END-->

      {block:Link}<!--LINK POSTS-->
      <div class="post link">
        <a href="{URL}">{Name}</a>
        {block:Description}<br>
          {Description}
        {/block:Description}
      </div>
      {/block:Link}<!--LINK POSTS END-->

    {/block:Posts}<!--TUMBLR POST STOP-->
  </div><!--POST CONTAINER END-->
  <footer>
    <a href="http://viewtwo-theme.tumblr.com" id="hi">
      ViewTwo
    </a>
  </footer>
  </body>

</html>
```
