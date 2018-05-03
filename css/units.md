# css units

잘 안쓰던 css 단위와 최근 알게된 단위 몇 가지를 간략하게 정리 하고자 한다.

0. em,rem

    >  rem은 em과 비슷 하게 보일 수 있다.
    >
    >  차이는 em은 current Elememt font-size px (default - 16px) 을 기준으로 삼아 지정하는 단위이다
    >
    >  rem은 body font-size를 기준으로 삼아 지정하는 단위이다.

    <br>

    **em**
    ```
    <div class="box"></div>
    ```
    ```
    .box {
        font-size: 15px;
        padding: 1em; // padding: 15px;
    }
    ```
    <br>

    **rem**
    ```
    <body>
        <div class="box"></div>
    </body>
    ```
    ```
    body {
        font-size: 13px;
    }

    box {
        font-size: 1.3em; // font-size: 1.3 * 13px;
    }
    ```
    <br>

0. vh, vw
    > **vh** 요소는 바로 위의 부모 엘리먼트의 영향을 받아 부모 높이의 100분의 1 값이 1vh가 된다.
    >
    > 예를 들어 부모의 높이가 1000px이라면 1vh는 100px이 된다.
    >
    > 마찬가지로 **vw**은 부모의 너비가 기준이되고 부모의 너비 100분의 1값이 1vm이 된다.
    >
    > 즉, 100vm 100vh 는 최대 높이값 최대 너비값이 된다.

    ```
    <div class="box"></div>
    ```
    ```
    .box {
        width: 100vw;
        width: 100vh;
    }
    ```
    <br>
0. vmin, vmax
    > vh, vw와 비슷 원리의 단위이다.
    >
    > 너비값과 높이값에 최소값과 최대값을 지정 해 줄 수 있다.
    > 예를 들어 브라우저가 1000px 너비, 700px높이 일때 1vmin은 7px이 되고 1vmax는 10px이 된다.
    >
    > 반대로 800px 너비, 1100px 높이일대는 1vmin은 8px, 1vmax는 11px이 됩니다.

    ```
    .box {
        height: 100vmin;
        width: 100vmin;
    }
    ```