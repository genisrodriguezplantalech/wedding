<script>
    import { data } from './assets/gyc.json';
    import CountDown from './components/CountDown.svelte';
    import Story from './components/Story.svelte';
    import BasicSection from './components/BasicSection.svelte';
    import Instagram from './components/Instagram.svelte';
    import Credits from './components/Credits.svelte';

    const { metadata, countdown, story, confirmation, location, songs, instagram } =
        data;

    document.title = metadata?.title || document.title;
</script>

<CountDown limitDate={new Date(countdown.weddingDate)} />

<!-- location -->
<BasicSection
    titleIconChurch=true
    title={location.title}
    description={location.description}
    buttonText={location.buttonText}
    buttonExternalUrl={location.src}
/>

<!-- confirmation -->
<BasicSection
    titleIconList=true
    title={confirmation.title}
    description={confirmation.description}
    buttonText={confirmation.buttonText}
    buttonExternalUrl={confirmation.src}
/>

<Story
    titleIconBook=true
    title={story.title} 
    description={story.description} 
    photos={story.photos} 
/>

<!-- songs -->
<BasicSection
    songs=true
    titleIconMusic=true
    title={songs.title}
    description={songs.description}
    buttonText={songs.buttonText}
    buttonExternalUrl={songs.src}
/>

<Instagram
    hashtag={instagram.hashtag}
    hashtagSrc={instagram.hashtagSrc}
    buttonText={instagram.buttonText}
    backgroundSrc={instagram.backgroundSrc}
/>

<Credits
/>