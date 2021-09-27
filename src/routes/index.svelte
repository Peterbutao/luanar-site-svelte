<svelte:head>    
    <title>luanar timetable | HOME</title>
    <meta name="description" content="luanar bssy timetable">
    <meta name="author" content="peter butao">

</svelte:head>
<article>
    <header>
        <p>BSSY TIMETABLE FOR BSSY STUDENTS</p>
    </header>
    <main>
        <h1>DOWNLOAD</h1>
        <div class="links">
            <div class="lnk">

                <a href="./src" download="bssy timetable" class="card">
                    <div class="cd">
                        <div class="text">
                            <h1>
                                <span>1.0.0</span>
                                <span style="color: var(--bl)">LTS</span>
                            </h1>
                            <p>6/09/21</p>
                        </div>
                        <div class="svg">
                            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="110" height="110" viewBox="0 0 110 110"><defs><clipPath id="a"><rect width="16" height="16" fill="none"/></clipPath></defs><g transform="translate(-259 -236)"><rect width="110" height="110" transform="translate(259 236)" fill="rgba(38,153,251,0.05)"/><g transform="translate(306 282)" clip-path="url(#a)"><path d="M8,0,6.545,1.455l5.506,5.506H0V9.039H12.052L6.545,14.545,8,16l8-8Z" transform="translate(16) rotate(90)" fill="rgba(38,153,251,0.53)"/></g></g></svg>

                        </div>
                    </div>
                </a>
            </div>
        </div>
    </main>
</article>

<style lang="scss">
        @mixin font($c, $s, $w) {
        font-family:Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing:antialiased;
        -moz-osx-font-smoothing:grayscale;
        color:$c;
        font-size: $s;
        font-weight:$w;

    }
    article{
        padding: 15vh 0;
        padding-left: 10px;
        padding-right: 10px;
        background: var(--bc);
        header{
            p{
                @include font(var(--tc), 0.95rem, 500);
            }
        }
        main{
            padding:20px 0px;
            h1{
                @include font(var(--tc), 0.95rem, 800);
            }
            .links{
                .lnk{

                    a{
                        text-decoration: none;
                        padding:0;
                        margin:0;
                        .cd{
                            background: var(--fm);
                            display: flex;
                            align-items: center;
                            justify-content: space-between;
                            .text{
                                padding: 10px;
                                h1{
                                    @include font(var(--tc), 1.5rem, 500);
                                }
                                p{
                                    @include font(var(--tc), 0.7rem, 100);
                                }
                            }
                        }
                    }
                }
            }
        }
    }
</style>