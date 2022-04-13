<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            text-align: center;
        }
        .starInner{
            color: #95a5a6;
            cursor: pointer;
        }
        .nstars [result]{
            padding-left: 7px;
        }
        @keyframes starAnimScale{
            0%,100%{transform: scale(1);}
            50%{transform: scale(1.2);}
        }
        @keyframes starAnimRotate{
            0%{transform: rotate(0deg);}
            100%{transform: rotate(360deg);}
        }
        @keyframes starAnimColor{
            0%,100%{color: #f39c12;}
            50%{color: red;}
        }
        .nstars[stars][animation="scale"].anim .starInner span[nstar]{
            animation: starAnimScale .5s linear 0s 1;
            display: inline-block;
        }
        .nstars[stars][animation="rotate"].anim .starInner span[nstar]{
            animation: starAnimRotate .5s linear 0s 1;
            display: inline-block;
        }
        .nstars[stars][animation="color"].anim .starInner span[nstar]{
            animation: starAnimColor .5s linear 0s 1;
            display: inline-block;
        }
        .nstars[stars][levelAnim].anim .starInner span[nstar]{
            animation-delay: 0s !important;
        }
        .nstars[stars][levelAnim].anim .starInner .starInner span[nstar]{
            animation-delay: .2s !important;
        }
        .nstars[stars][levelAnim].anim .starInner .starInner .starInner span[nstar]{
            animation-delay: .4s !important;
        }
        .nstars[stars][levelAnim].anim .starInner .starInner .starInner .starInner span[nstar]{
            animation-delay: .6s !important;
        }
        .nstars[stars][levelAnim].anim .starInner .starInner .starInner .starInner .starInner span[nstar]{
            animation-delay: .8s !important;
        }
        .nstars[stars] .starInner{
            color: #f39c12;
        }
        .nstars:not([locked='true']):hover .starInner{
            color: #95a5a6;
        }
        .nstars:not([locked='true']) .starInner:hover{
            color: #f39c12 !important;
        }
        .nstars[stars="0"] .starInner{
            color: #95a5a6;
        }
        .nstars[stars="0"] .starInner span[nstar]{
            animation: none !important;
        }
        .nstars[stars="0"] [result]::before{
            content: "";
        }
        .nstars[stars="1"] .starInner .starInner{
            color: #95a5a6;
        }
        .nstars[stars="1"] .starInner .starInner span[nstar]{
            animation: none !important;
        }
        .nstars[stars="1"] [result]::before{
            content: "😭";
        }
        .nstars[stars="2"] .starInner .starInner .starInner{
            color: #95a5a6;
        }
        .nstars[stars="2"] .starInner .starInner .starInner span[nstar]{
            animation: none !important;
        }
        .nstars[stars="2"] [result]::before{
            content: "😟";
        }
        .nstars[stars="3"] .starInner .starInner .starInner .starInner{
            color: #95a5a6;
        }
        .nstars[stars="3"] .starInner .starInner .starInner .starInner span[nstar]{
            animation: none !important;
        }
        .nstars[stars="3"] [result]::before{
            content: "🙂";
        }
        .nstars[stars="4"] .starInner .starInner .starInner .starInner .starInner{
            color: #95a5a6;
        }
        .nstars[stars="4"] .starInner .starInner .starInner .starInner .starInner span[nstar]{
            animation: none !important;
        }
        .nstars[stars="4"] [result]::before{
            content: "😄";
        }
        .nstars[stars="5"] [result]::before{
            content: "😍";
        }
        .nstars[emoji="false"] [result]::before{
            content: "" !important;
        }
    </style>
</head>
<body>
    <strong>Default: </strong>
    <span class="nstars">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>


    <br><br><br>

    <div style="direction: rtl;">
        <strong>Default (RTL): </strong>
        <span class="nstars">
            <span class="starInner">
                <span nstar="1"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="2"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="3"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="4"><i class="fa fa-star"></i></span>
                            <span class="starInner">
                                <span nstar="5"><i class="fa fa-star"></i></span>
                                <span result></span>
                            </span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </div>


    <br><br><br>


    <strong>No Emoji: </strong>
    <span class="nstars" emoji="false">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>


    <br><br><br>

    <strong>With Value: </strong>
    <span class="nstars" stars="3">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>

    <br><br><br>

    <div style="direction: rtl;">
        <strong>With Value (RTL): </strong>
        <span class="nstars" stars="2">
            <span class="starInner">
                <span nstar="1"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="2"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="3"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="4"><i class="fa fa-star"></i></span>
                            <span class="starInner">
                                <span nstar="5"><i class="fa fa-star"></i></span>
                                <span result></span>
                            </span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </div>


    <br><br><br>

    <strong>Locked: </strong>
    <span class="nstars" stars="3" locked="true">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>

    <br><br><br>

    <strong>Scale Animation: </strong>
    <span class="nstars" animation="scale" stars="3">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>

    <br><br><br>

    <strong>Rotate Animation: </strong>
    <span class="nstars" animation="rotate" stars="3">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>

    <br><br><br>

    <strong>Color Animation: </strong>
    <span class="nstars" animation="color" stars="3">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>

    <br><br><br>

    <strong>Scale Animation (LEVEL ACTIVE): </strong>
    <span class="nstars" animation="scale" levelAnim stars="3">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>

    <br><br><br>

    <strong>Rotate Animation (LEVEL ACTIVE): </strong>
    <span class="nstars" animation="rotate" levelAnim stars="3">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>

    <br><br><br>

    <strong>Color Animation (LEVEL ACTIVE): </strong>
    <span class="nstars" animation="color" levelAnim stars="3">
        <span class="starInner">
            <span nstar="1"><i class="fa fa-star"></i></span>
            <span class="starInner">
                <span nstar="2"><i class="fa fa-star"></i></span>
                <span class="starInner">
                    <span nstar="3"><i class="fa fa-star"></i></span>
                    <span class="starInner">
                        <span nstar="4"><i class="fa fa-star"></i></span>
                        <span class="starInner">
                            <span nstar="5"><i class="fa fa-star"></i></span>
                            <span result></span>
                        </span>
                    </span>
                </span>
            </span>
        </span>
    </span>

    <br><br><br><br><br><br>


    <script src="https://code.jquery.com/jquery-3.6.0.min.js" integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>
    <script defer src="https://use.fontawesome.com/releases/v5.15.4/js/all.js" integrity="sha384-rOA1PnstxnOBLzCLMcre8ybwbTmemjzdNlILg8O7z1lUkLXozs4DHonlDtnE7fpc" crossorigin="anonymous"></script>
    <script>
        $("[nstar]").click(function(){
            if($(this).parents(".nstars").attr("locked")!="true"){
                $(this).parents(".nstars").attr("stars",$(this).attr("nstar"));
                $(this).parents(".nstars").addClass("anim");
                setTimeout(()=>{
                    $(this).parents(".nstars").removeClass("anim");
                },1300)
            }
        });
    </script>
</body>
</html>
