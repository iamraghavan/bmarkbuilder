<svelte:head>

<title>Galley - BenchMark Builders - Chennai</title>

    <meta name="title" content="Gallery - Imagine your dream home! BenchMark Builders brings it to life.">
<meta name="description" content="Imagine your dream home! BenchMark Builders brings it to life. Trust us for quality construction. Your dream home is just a step away!">
<meta name="keywords" content="warehouse construction in chennai, construction in chennai, plots for sale in chennai,builders in chennai,plots in chennai,best builders in chennai,top builders in chennai,construction company,building construction,home construction,building company,building construction company in chennai,construction company in chennai,chennai construction ,constructions in chennai">
<meta name="robots" content="noindex, nofollow">
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<meta name="language" content="English">
<meta name="revisit-after" content="2 days">
<meta name="author" content="Bumble Bees IT Solutions">

</svelte:head>

<script>

  
      export let activePage = "Home"; 


      let videos = [];
  
  // Replace 'YOUR_API_KEY' and 'YOUR_CHANNEL_ID' with actual values
  const apiKey = 'AIzaSyC03Ole8PT6sQzwafGLPdUaYdPAt88BfsA';
  const channelId = 'UCR5WZKLR2pW3D3rH-_A0Ldg';
  const maxResults = 9;

  $: {
    // Fetch videos from your YouTube channel
    fetch(`https://www.googleapis.com/youtube/v3/search?part=snippet&channelId=${channelId}&maxResults=${maxResults}&order=date&type=video&key=${apiKey}`)
      .then(response => response.json())
      .then(data => {
        // Extract video information
        videos = data.items.map(item => ({
          title: item.snippet.title,
          thumbnail: item.snippet.thumbnails.medium.url,
          videoId: item.id.videoId,
        }));
      });
  }


  
    </script>
    
    <div class="rs-breadcrumbs img1">
      <div class="container">
        <div class="breadcrumbs-inner">
          <h1 class="page-title">
            Gallery - Benchmark Builders
          </h1>
          
          <ul class="breadcrumbs-area">
            <li title={`Go to ${activePage}`}>
              <a class:active={activePage === "Home"} href="/">Home</a>
            </li>
            <li>Gallery</li>
          </ul>
        </div>
      </div>
    </div>


  
  
  <div class="rs-gallery gallery-style1 pt-120 pb-120 md-pt-80 md-pb-80">
    <div class="container">
      <div class="row">
        {#each videos as { title, thumbnail, videoId }}
          <div class="col-lg-4 col-md-6 mb-30">
            <div class="gallery-item">
              <div class="gallery-icon">
                <a class="video-popup" href={`https://www.youtube.com/watch?v=${videoId}`}>
                  <img src={thumbnail} alt={title}>
                </a>
              </div>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
  