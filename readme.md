> Không phải thuộc tính nào cũng có transition, ví dụ như display sẽ không có.
> transition: transform 3s 2s delay;
> @keyframes expand {
    0% {
        width: 0px;
    }

    100%{
        width: 100px;
    }
}

animation: expand 2s forwards

> Khi responsive thì font chữ sử dụng em ( 1em = kích thước font chữ cụ thể của parent)

> Khi responsive thì width và height nên dùng % ( liên quan đến kích thước tương ứng của parent)

> Grid
.container {
    display: grid;
    grid-template-column: 25% 50% 25%;
    grid-template-row: 25% 25% 25% 25;
}

.items {
    grid-colums-start: 1;
    grid-column-end: 2;
    grid-row-start: 1;
    grid-row-end: 2;
}

> strick: Responsive dùng grid:
.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}

> in major browers, default margin is 8px, so if you want to change it, you can do this:
body {
    margin: 0px;
}

> using grid-area to create detail layout
.container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 20vh 20vh 20vh 20vh 20vh;
    grid-template-areas: 
        "header header"
        "main about"
        "main news"
        "main ads"
        "main links"
        "main footer";
}

.footer {
    background-color: rgb(0, 102, 128);
    grid-area: footer;
}

> cannot verical align with margin: auto, because traditional web is concern on horrizontal, not sp vertical, ( that is my thought :)) )

> Bình thường thì width = chiều rộng của content + kích thước padding
box-sizing:
+ border-box: width bao gồm cả nội dung, padding, border nhưng không bao gồm margin
muốn áp dụng border-box thì element phải có specific width and height;

> Khi muon ap dung z-index thi position phai khac mac dinh !