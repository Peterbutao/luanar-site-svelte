<script>
	import Router, {link} from "svelte-spa-router";
	import Home from "./routes/index.svelte";


	$: open = false;
</script>
<Router routes={{
	"/":Home
}}/>



<section  id="layout">
    <nav class="nav-one">
        <div class="nv">
            <div on:click={() => {open = !open}} class="menu">
                <div class="line-1"></div>
                <div class="line-2"></div>
                <div class="line-3"></div>
            </div>
            <div class="brand">
                <a href="/">
                    <span>             
                        <img src="./assets/logo.png" width="50px" alt="logo">
                    </span>
                    <span>
                        <h1>LUANAR </h1>
                    </span>    
              </a>        
            </div>
            <div class:open={open} on:click={() => {open = !open}} class="nav-bar">
                <ul on:click={() => {open = open}} class="navlist">
                    <li><a href="https://github.com/Peterbutao/luanar-site-svelte.git">GET INVOLVED</a></li>
                    <li><a href="https://github.com/Peterbutao/luanar-site-svelte.git">DOCS</a></li>
                    <li><a href="https://github.com/Peterbutao/luanar-site-svelte.git/licence">LICENCE</a></li>
                    <li><a href="tel://0880164455">CONTACT</a></li>            

                </ul>
            </div>
        </div>
    </nav>
    <main class="content">
        <slot></slot>
    </main>
    <footer class="foot">
        <div class="ft">

            <div class="brand">
                <span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="90" height="90" viewBox="0 0 90 90"><g transform="translate(-17 -562)"><rect width="90" height="90" transform="translate(17 562)" fill="#d3dee7"/><text transform="translate(22 615)" fill="#2698fb93" font-size="24" font-family="SegoeUI-Bold, Segoe UI" font-weight="700"><tspan x="0" y="0">BUTAO</tspan></text></g></svg>
                </span>
                <span class="text">
                    <h1>BUTAO DEV</h1>
                    <p>&copy BUTAO UX / UI DEV | 2021</p>
                </span>
            </div>
            <ul class="navlist">
                <li><a href="https://github.com/Peterbutao/luanar-site-svelte.git">GET INVOLVED</a></li>
                <li><a href="tel://0880164455">CONTACT</a></li>            

            </ul>
            
           


        </div>
    </footer>

</section>

<style lang="scss">
    :global(body) {
        color: blue;
        background: var(--nv);
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    :root{
        --bc:hsl(0, 0%, 95%);
        --nv:hsl(0, 0%, 92%);
        --tc:hsl(0, 0%, 25%);
        --lc:seashell;
        --bl:#2699fb;
        --fb:#EBF1F6;
        --fm: #d3dee7;
        --tbc: #d3dee7;
    }
   
    @mixin font($c, $s, $w) {
        font-family:Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing:antialiased;
        -moz-osx-font-smoothing:grayscale;
        color:$c;
        font-size: $s;
        font-weight:$w;

    }
    #layout{
        .nav-one{

            z-index: 99;
            position: fixed;
            width: 100%;
            background: var(--nv);
            top: 0;
            left: 0;
            .nv{
                box-shadow: #0000002c 0px 3px 11px 0px;
                display: flex;
                align-items: center;
                background: var(--nv);
                .menu{
                    padding: 20px 10px;
                    position: relative;
                    z-index: 99;
                    display: none;
                    div{
                        width: 20px;
                        height: 3px;
                        background: var(--tc);
                     
                    }
                    .line-2{
                        margin: 5px 0px;
                        width: 12px;
                    }
                   
                    
                }
                .brand{
                    padding: 0px 10px;
                    a{
                        display: flex;
                        align-items: center;
                        padding: 3px 15px;
                        text-decoration: none;
                        h1{
                            padding: 0px 15px;
                            @include font(var(--tc), 1rem, 500);  
                        }
                    }
                }
                .open{
                    width: 100% !important;
                    transition: all 1s ease !important;
                    opacity: 100% !important;
                    pointer-events: all !important;
                }
                .nav-bar{
                    z-index: 9;
                    position: fixed;
                    top: 0;
                    left: 0;
                    background: #0000001e;
                    opacity: 0;
                    width:0;
                    height: 100vh;
                    overflow: hidden;
                    padding: 0;
                    transition: all 0.5s ease;
                    pointer-events: none;

                    .navlist{
                    
                        background: var(--fb);
                        height: 100vh;
                        width: 65%;
                    }
                    ul{
                        margin: 0;
                        padding: 20vh 0;
                        li{
                            list-style: none;
                            padding: 20px 10px;
                            a{
                                text-decoration: none;
                                @include font(var(--tc), 0.95rem, 500);
                                
                                span{
                                    padding: 0px 5px;
                                    svg{
                                        filter: grayscale(50%);
                                    }
                                }
                                
                            }
                            &:hover{
                                background: #2699fb;
                            }
                        }
                    }
                }
            }

        }
        .foot{
            border-top: solid rgba(0, 0, 0, 0.309) 0.9px;   
            position: relative;
            bottom: 0;
            height: 10vh;
            background: var(--nv);
            
            .ft{
                padding: 0px 20px;
                display: flex;
                justify-content: space-between;
                flex-direction:column;
                ul{
                        margin: 0;
                        padding:0;
                        padding-top: 20px;
                        
                        li{
                            list-style: none;
                            padding: 10px 0px;
                        
                            a{
                                text-decoration: none;
                                @include font(var(--tc), 0.95rem, 300);
                                
                            
                                
                            }
                            
                        }
                    }
                .brand{
                    display: flex;
                    .text{
                        padding-left: 20px;
                    }
                    h1{
                       @include font(var(--tc), 0.95rem, 800);
                    }
                    p{
                        @include font(var(--bl), 0.8rem, 500)
                    }
                }
               
            }

        }
    }
</style>