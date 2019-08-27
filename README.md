# ejemplo-pagina
ejemplo pagina

<p style="color: green">hola</p>
<p id="receiver"></p>
<button id="send">Enviar MSG a Principal</button>

<script type="text/javascript">
document.getElementsByTagName('p')[0].style.color = 'red';
function bindEvent(element, eventName, eventHandler) {
       	if (element.addEventListener) {
               	element.addEventListener(eventName, eventHandler, false);
      	} else if (element.attachEvent) {
               	element.attachEvent('on' + eventName, eventHandler);
       	}
}
	
var sendMessage = function (msg) {
	window.parent.postMessage(msg, '*');
};

var messageButton = document.getElementById('send');

bindEvent(messageButton, 'click', function (e) {
	var random = Math.random();
	sendMessage('segunda ' + random);
});
</script>

