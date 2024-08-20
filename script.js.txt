function generateHexagram() {
    let yaos = [];
    for (let i = 1; i <= 6; i++) {
        let yao = document.getElementById(`yao${i}`).value.trim();
        yaos.push(yao === "1" ? "———" : yao === "0" ? "— —" : "");
    }
    if (yaos.includes("")) {
        alert("请输入有效的爻值：1（阳爻）或0（阴爻）");
        return;
    }
    document.getElementById("hexagram").innerHTML = yaos.reverse().join("<br>");
}
