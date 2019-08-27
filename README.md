# ejemplo-pagina
ejemplo pagina

<p style="color: green">hola</p>
<p id="mensaje"></p>
<button id="send">Enviar MSG a Principal</button>

<script type="text/javascript">
	document.getElementsByTagName('p')[0].style.color = 'red';
	window.onload = function() {
  	
  var receiver = document.getElementById('receiver').contentWindow;

  	
  var btn = document.getElementById('send');


  function sendMessage(e) {

   e.preventDefault();

   
   receiver.postMessage('Hello Treehouse!', '*');
  }

  
  
  btn.addEventListener('click', sendMessage);
}
</script>

