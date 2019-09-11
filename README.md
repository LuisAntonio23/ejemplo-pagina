# ejemplo-pagina
ejemplo pagina

<p style="color: green">hola</p>
<p id="receiver"></p>
<button id="send">Enviar MSG a Principal</button>
<a href=" https://luisantonio23.github.io/prueba-pag-2/"><button id="next">siguiente pag</button></a>

<script type="text/javascript">
window.onload = function() {
	function receiveMessage(e) {
		
		var styleSheet = document.createElement('style')
		styleSheet.innerHTML = e.data[0];
		document.body.appendChild(styleSheet);
		
		if(e.data[1] == "getUrlLocation"){
			sendMessage('' + document.location);	
		}	
	}
	
	var sendMessage = function(msg){
		window.parent.postMessage(msg, '*');
	};
	
	window.addEventListener('message', receiveMessage);
}
</script>
