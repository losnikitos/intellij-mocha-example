## Table

<style>
    table {
        border-spacing: 5px;
    }

    body {
        font-family: "Textbook New", "Helvetica Neue", "Helvetica", sans-serif;
    }

    td {
        padding: 10px 20px;
    }

    .desc {
        padding-left: 10px;
    }

    .box {
        border-radius: 10px;
        font-weight: 700;
    }

    .blue1 {
        background-color: #3d62b6;
    }

    .blue2 {
        background-color: #95c2ed;
    }
</style>
<table>
    <tr>
        <td rowspan="3" class="box blue1">gulp</td>
        <td class="box blue2">gulp deps</td>
        <td class="desc">npm i<br>
            cd server && npm i<br>
            cd static && npm i<br>
            cd static && bower i
        </td>
    </tr>
    <tr>
        <td class="box blue2">gulp static</td>
        <td class="desc">cd static && enb make</td>
    </tr>
    <tr>
        <td class="box blue2">gulp run</td>
        <td class="desc">Запуск на порту, на сокете или в коксе</td>
    </tr>
</table>
