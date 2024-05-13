<p>At&eacute; o presente momento o Formul&aacute;rio do Google Docs (Google Forms) n&atilde;o permite coletar coordenadas geogr&aacute;ficas de latitude e longitude. Por essa raz&atilde;o, preparei esse c&oacute;digo HTML utilizando bibliotecas javascript para criar um mapa interativo, onde os usu&aacute;rios podem fornecer a localiza&ccedil;&atilde;o para um formul&aacute;rio do Google Forms. Embora na programa&ccedil;&atilde;o existam estrat&eacute;gias mais eficientes para coletas de coordenadas, esse c&oacute;digo pretende ser &uacute;til para quem n&atilde;o tem dom&iacute;nio de programa&ccedil;&atilde;o mas&nbsp;possui interesse em fazer um formul&aacute;rio no Google Forms, adicionando&nbsp;um passo anterior ao preenchimento do formul&aacute;rio no Google Forms. No entanto &eacute; ncess&aacute;rio saber hospedar um c&oacute;digo HTML em um servidor com HTTPS.</p>
<p>(<a href="https://docente.ifsc.edu.br/joao.quoos/labMAGe/html/formulariolatlong.html" target="_blank">LINK DEMO</a>)</p>
<hr />
<p><a href="#apresentacao"><strong>1) Apresenta&ccedil;&atilde;o dos recursos</strong></a></p>

<p><a href="#como"><strong>2) </strong></a><strong><a href="#">Pr&eacute;-requisitos e como utilizar</a></strong></p>

<hr />
<p><strong><a id="apresentacao" name="apresentacao"></a>Apresenta&ccedil;&atilde;o dos recursos</strong></p>

<p><br />
<strong>C&oacute;digo JavaScript:</strong></p>

<p>Esse HTML modelo (formulariolatlong.html) possui&nbsp;c&oacute;digos JavaScript que auxiliam no processo. Ele usa a biblioteca <a href="https://leafletjs.com/" target="_blank">Leaflet </a>para criar um mapa interativo. Ele tamb&eacute;m usa a biblioteca <a href="https://sweetalert2.github.io/" target="_blank">SweetAlert2</a> para exibir alertas de confirma&ccedil;&atilde;o e a biblioteca <a href="https://jquery.com/" target="_blank">jQuery </a>para manipula&ccedil;&atilde;o de DOM e manipula&ccedil;&atilde;o de eventos.</p>

<p><strong>Estrat&eacute;gia do Formul&aacute;rio:</strong></p>

<p>O formul&aacute;rio &eacute; usado para exibir e enviar as coordenadas do marcador. Quando o marcador &eacute; movido no mapa, os campos de entrada do formul&aacute;rio s&atilde;o atualizados com a nova latitude e longitude do marcador. Quando o bot&atilde;o &ldquo;Enviar&rdquo; &eacute; clicado, os valores de latitude e longitude s&atilde;o enviados para a URL especificada, que &eacute; o formul&aacute;rio do Google Forms.</p>

<p><strong>Fun&ccedil;&otilde;es do C&oacute;digo:</strong></p>

<ol>
	<li>
	<p><strong>Inicializa&ccedil;&atilde;o do Mapa e do Marcador:</strong>&nbsp;O mapa &eacute; inicializado com uma camada de mapa <a href="https://www.openstreetmap.org/#map=4/-15.13/-53.19" target="_blank">OpenStreetMap </a>e um marcador que pode ser arrastado. O marcador &eacute; inicialmente colocado no centro de uma &aacute;rea que no caso desse c&oacute;digo &eacute; Santa Catarina.</p>
	</li>
	<li>
	<p><strong>Atualiza&ccedil;&atilde;o das Coordenadas do Marcador:</strong>&nbsp;Quando o marcador &eacute; arrastado e solto, a latitude e longitude do marcador s&atilde;o atualizadas nos campos de entrada do formul&aacute;rio.</p>
	</li>
	<li>
	<p><strong>Troca de Mapa:</strong>&nbsp;Quando o bot&atilde;o &ldquo;Trocar Mapa&rdquo; &eacute; clicado, o mapa alterna entre tr&ecirc;s camadas de mapa: OpenStreetMap, uma imagem de sat&eacute;lite e um mapa de aquarela.</p>
	</li>
	<li>
	<p><strong>Obten&ccedil;&atilde;o da Localiza&ccedil;&atilde;o:</strong>&nbsp;Quando o bot&atilde;o &ldquo;Obter Localiza&ccedil;&atilde;o&rdquo; &eacute; clicado, a localiza&ccedil;&atilde;o atual do usu&aacute;rio &eacute; obtida usando o GPS. O marcador &eacute; movido para essa localiza&ccedil;&atilde;o e o mapa &eacute; centrado nessa localiza&ccedil;&atilde;o.Essa fun&ccedil;&atilde;o exige que o c&oacute;digo HTML esteja hospedado em um Servidor Seguro, com recurso HTTPS.</p>
	</li>
	<li>
	<p><strong>Geocoder:</strong>&nbsp;Um controle de geocoder &eacute; adicionado ao mapa no canto superior direito, que permite ao usu&aacute;rio pesquisar um endere&ccedil;o. Quando um endere&ccedil;o &eacute; selecionado, o marcador &eacute; movido para essa localiza&ccedil;&atilde;o e o mapa &eacute; centrado nessa localiza&ccedil;&atilde;o.</p>
	</li>
	<li>
	<p><strong>Mover o Marcador com Dois Cliques:</strong>&nbsp;Quando o usu&aacute;rio d&aacute; um duplo clique em qualquer lugar do mapa, o marcador &eacute; movido para a localiza&ccedil;&atilde;o clicada.</p>
	</li>
	<li>
	<p><strong>Envio do Formul&aacute;rio:</strong>&nbsp;Quando o formul&aacute;rio &eacute; enviado, primeiro verifica se os campos de latitude e longitude est&atilde;o vazios. Se estiverem vazios, um alerta &eacute; exibido. Se n&atilde;o estiverem vazios, um alerta de confirma&ccedil;&atilde;o &eacute; exibido. Se o usu&aacute;rio confirmar, os dados s&atilde;o enviados para a URL especificada.</p>
	<hr />
	<p><strong><a id="como" name="como"></a>2) Pr&eacute;-requisitos e como utilizar</strong></p>
	</li>
</ol>

<p>2.1) Obter uma URL&nbsp;</p>

<ul>
	<li>Para isso adicione no seu formul&aacute;rio do Google Forms dois campos, um para <strong>Latitude </strong>e outro para <strong>Longitude</strong>. Ex.:</li>
</ul>

<p style="text-align:center"><img alt="" height="508" src="https://i.ibb.co/cTBPtTY/image.png" width="859" /></p>

<ul>
	<li>Em seguida no meu de op&ccedil;&otilde;es &eacute; necess&aacute;rio <strong>Gerar link j&aacute; preenchido automaticamente</strong>. isso vai criar uma URL e apresentar dados que ser&atilde;o utilizados no c&oacute;digo HTML.</li>
</ul>

<p style="text-align:center"><img alt="" height="300" src="https://i.ibb.co/gFFRSBS/image.png" width="539" /></p>

<p>Preencha os campos de latitude e longitude como no exemplo, para obter o link. Depois de preenchido clique no bot&atilde;o gerar link. Em seguida clique no bot&atilde;o copiar link.</p>

<p style="text-align:center"><img alt="" height="410" src="https://i.ibb.co/xYbVGmy/image.png" width="748" /></p>

<p>&nbsp;</p>

<p>Esse&nbsp;link agora ser&aacute; utilizado como refer&ecirc;ncia para alterar o c&oacute;digo HTML.</p>

<p>Link de exemplo:<br />
<a href="https://docs.google.com/forms/d/e/1FAIpQLSfJZ_yAxdESNgpWrSqTcwIPRvQ-ovXi_XEKr4aoZVnei5e6tg/viewform?usp=pp_url&amp;entry.1958008891=-29.5&amp;entry.1942728764=-48.5">https://docs.google.com/forms/d/e/<em>1FAIpQLSfJZ_yAxdESNgpWrSqTcwIPRvQ-ovXi_XEKr4aoZVnei5e6tg</em>/viewform?usp=pp_url&amp;<em>entry.1958008891</em>=-29.5&amp;<em>entry.1942728764</em>=-48.5</a></p>

<p>Onde&nbsp;<em><span style="color:#696969">1FAIpQLSfJZ_yAxdESNgpWrSqTcwIPRvQ-ovXi_XEKr4aoZVnei5e6tg</span>&nbsp;</em>&eacute; o id do formul&aacute;rio no google Docs,&nbsp;<em><span style="color:#696969">entry.1958008891</span> </em>&eacute; o id da Latitude (lat) e o<em> <span style="color:#696969">entry.1942728764</span></em>&nbsp;o id de longitude (lng).</p>

<p>Identifique no seu link esses dados, pois ser&atilde;o necess&aacute;rios para alterar o&nbsp;c&oacute;digo HTML de&nbsp;<strong>formulariolatlong.html </strong>.</p>

<p>Troque os respectivos c&oacute;digos dentro do c&oacute;digo HTML. Salve e hospede esse arquivo em um Servidor HTTPS. Pois s&oacute; assim as fun&ccedil;&otilde;es de geolocaliza&ccedil;&atilde;o ir&atilde;o funcionar no c&oacute;digo.&nbsp;</p>

<p><code>// aqui s&atilde;o realizadas tr&ecirc;s modifica&ccedil;&otilde;es. Coloque a URL fornecidade pelo Google Forms Preenchido conmforme modelo e altere os valores de entry para lat de latitude e lng de longitude var url = &#39;https://docs.google.com/forms/d/e/1FAIpQLSULRDOGOOGLEFORMShJivZjKaI-fCwSoXJZBBBBBBJYCZNQ0-AAAAAAA/viewform?usp=pp_url&amp;entry.912345678=&#39; + lat + &#39;&amp;entry.123456789=&#39; + lng;</code></p>

<p>A partir de agora, ao abrir esse HTML no browser do seu celular voc&ecirc; poder&aacute; obter as coordenadas geogr&aacute;ficas anteriormente ao preenchimento do seu Google Docs.</p>

<hr />
<p>Autor:<br />
Prof. Dr. Jo&atilde;o Henrique Quoos<br />
IFSC c&acirc;mpus Garopaba<br />
MAGe - Laborat&oacute;rio de Meio Ambiente e Geom&aacute;tica<br />
&nbsp;</p>
