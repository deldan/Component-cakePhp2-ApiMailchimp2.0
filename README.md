Proyecto para cakePhp V2.x
Componente conexión api Mailchimp V2.0


pasos de instalación

1.Añadir a los archivos de la carpeta components en app/Controller/Components de cakePhp.
2.Llamar desde cualquier controllador var $components=array('Mailchimp');
3.Crear una función utilizando el componente. (ejemplo listado de listas)

	3.A Listas

	$this->Mailchimp->api('API_KEY');
	$lists = $this->Mailchimp->call('lists/list'));

	3.B Subscribir

	$this->Mailchimp->api('API_KEY');
	$result = $Mailchimp->call('lists/subscribe', array(
	                'id'                => 'b1234346',
	                'email'             => array('email'=>'deldan@example.com'),
	                'merge_vars'        => array('FNAME'=>'Del', 'LNAME'=>'Dan'),
	                'double_optin'      => false,
	                'update_existing'   => true,
	                'replace_interests' => false,
	                'send_welcome'      => false,
	            ));
	print_r($result);

