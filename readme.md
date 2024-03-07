const readline = require("readline");
const reader = readline.createInterface({
   input: process.stdin,
   output: process.stdout,
});
reader.question("Informe o valor da umidade atual em percentagem: ", umidade => {
   umidade = parseFloat(umidade);
   if (umidade > 60) {
       console.log("O ar está húmido.");
   } else if (umidade >= 30 && umidade <= 60) {
       console.log("O ar está seco.");
   } else {
       console.log("O ar está muito seco.");
   }
   reader.close();
});
