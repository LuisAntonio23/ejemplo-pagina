# ejemplo-pagina
ejemplo pagina

<p style="color: green">hola</p>
<p id="mensaje"></p>
<button id="send">Enviar MSG a Principal</button>

<script type="text/javascript">
	document.getElementsByTagName('p')[0].style.color = 'red';
	window.onload = function() {
  	// Get the window displayed in the iframe.
  	var receiver = document.getElementById('receiver').contentWindow;

  	// Get a reference to the 'Send Message' button.
  	var btn = document.getElementById('send');

  	// A function to handle sending messages.
  	function sendMessage(e) {
    	// Prevent any default browser behaviour.
    	e.preventDefault();

    	// Send a message with the text 'Hello Treehouse!' to the receiver window.
    	receiver.postMessage('Hello Treehouse!', '*');
  }

  // Add an event listener that will execute the sendMessage() function
  // when the send button is clicked.
  btn.addEventListener('click', sendMessage);
}
</script>

