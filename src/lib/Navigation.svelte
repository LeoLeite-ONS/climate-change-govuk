<script>
    import { page } from '$app/stores';
</script>

<aside>
    <nav>
        <ul>
            <li class:active={$page.path === '/'}>
                <a href=".">Overview</a>
            </li>
            <li class:active={$page.path === '/climate-weather'}>
                <a href="climate-weather">Climate and weather</a>
            </li>
            <li class:active={$page.path === '/emissions'}>
                <a href="emissions">Emissions</a>
            </li>
            <li class:active={$page.path === '/drivers'}>
                <a href="drivers">Drivers</a>
            </li>
            <li class:active={$page.path === '/impacts'}>
                <a href="impacts">Impacts</a>
            </li>
            <li class:active={$page.path === '/mitigation'}>
                <a href="mitigation">Mitigation</a>
            </li>
            <li class:active={$page.path === '/adaption'}>
                <a href="adaption">Adaption</a>
            </li>
        </ul>
    </nav>

    <hr />
    
    <nav>
        <ul>
            <li><a href="about-this-data">About this data</a></li>
            <li><a href="whats-new">What's new</a></li>
            <li><a href="download-data">Download data</a></li>
            <li><a href="developers-guide">Developer's guide</a></li>
        </ul>
    </nav>
</aside>

<style>
    aside {
        position: -webkit-sticky;
        position: sticky;
        width: 256px;
        margin: 0 0 24px;
    }

    hr {
        border: 0;
        border-bottom: 1px solid #B2B4B6;
        margin: 16px 0;
    }

    a {
        font-size: 16px;
        line-height: 24px;
        padding: 8px;
        text-decoration: none;
        border-left: 4px solid transparent;
        display: block;
    }

    a:hover {
        border-left: 4px solid #5694ca
    }

    li.active a {
        font-family: 'GDS Transport Bold', sans-serif;
        font-weight: 700;
        background: #F3F2F1;
        border-left: 4px solid #1d70b8;
    }

    nav:last-child a {
        font-size: 14px;
        line-height: 16px;
    }

    nav:last-child a:hover {
        border-left: 4px solid transparent;
        color: #003078;
    }
</style>