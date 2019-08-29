# ejemplo-pagina
ejemplo pagina

<p style="color: green">hola</p>
<p id="receiver"></p>
<button id="send">Enviar MSG a Principal</button>
<a href=" https://luisantonio23.github.io/prueba-pag-2/"><button id="next">siguiente pag</button></a>

<script type="text/javascript">
document.getElementsByTagName('p')[0].style.color = 'red';



function reciveMessage(e){
	if(e.data == 'getUrlLocation'){
		sendMessage('' + document.location);
	}
}

var sendMessage = function (msg) {
	window.parent.postMessage(msg, '*');
};

window.addEventListener('message',reciveMessage);
});
</script>

