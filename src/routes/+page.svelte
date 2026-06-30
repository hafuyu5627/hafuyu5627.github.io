<script lang="ts">
    import "./+page.scss";
    import TwitchLogo from "$lib/assets/icons/twitch.svelte";
    import TwitterLogo from "$lib/assets/icons/twitter.svelte";
    import YoutubeLogo from "$lib/assets/icons/youtube.svelte";
</script>

<h1 class="banner">羽冬</h1>

<div class="content">
    <div class="link-box">
        <a href="https://www.youtube.com/channel/UC4iC4rvanOLbLoZ-RK6gBXA">
            <div class="relative *:absolute size-8 group">
                <YoutubeLogo/>
                <div class="p-1 -left-4 -top-4 content-center text-center text-white text-lg/none font-bold bg-gray-600 group-hover:bg-gray-400 rounded-full transition-colors">主</div>
            </div>
        </a>
        <a href="https://www.youtube.com/channel/UCRraIyu0Dy52RBCJf7G35Ag">
        <div class="relative *:absolute size-8 group">
                <YoutubeLogo/>
                <div class="p-1 -left-4 -top-4 content-center text-center text-white text-lg/none font-bold bg-gray-600 group-hover:bg-gray-400 rounded-full transition-colors">副</div>
            </div>
        </a>
        <a href="https://www.twitch.tv/hafuyu5627"><TwitchLogo/></a>
        <a href="https://twitter.com/hafuyu5627"><TwitterLogo/></a>
    </div>
    <hr/>
    <p>
        大家好我是羽冬(羅: hafuyu; 平仮名: はふゆ)！
    </p>
    <p>
        我是一位遊戲實況主，目前以 Minecraft 生存系列為主
    </p>
</div>
