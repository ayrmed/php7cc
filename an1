<?php
header('Location: https://www.sanatusexo.com/blog/ok/');
?>
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"><title>Interpretación de resultado csh 1</title>
<META NAME="Title" CONTENT="Interpretación de resultado csh 1">
<META content="text/html; charset=iso-8859-1" http-equiv=Content-Type>
<META NAME="Subject" CONTENT="test">
<META NAME="Description" CONTENT="Interpretación de resultado de test de iief 1 tras realizar cuestionario de autoevaluación con preguntas sobre el rendimiento sexual">
<META NAME="Generator" CONTENT="html">
<META NAME="Language" CONTENT="Spanish">
<META NAME="Revisit" CONTENT="3 day">
<META NAME="Distribution" CONTENT="Global">
<META NAME="ROBOTS" CONTENT="NONE">

<?php
$email = $_POST['email']; 
$fecha = date("d-m-Y H:i"); 
$pais = $_POST['pais']; 
$provincia = $_POST['provincia']; 
$edad = $_POST['edad']; 
$aceptoavisolegal = $_POST['aceptoavisolegal'];
if(true === array_key_exists('submit', $_POST))
{
    mysql_connect("localhost","sanatus_admin2","ascensionqqq") or die(mysql_error()); 
    mysql_select_db("sanatus_pedidos") or die(mysql_error());
        $rResult = mysql_query(
        sprintf(
            "INSERT INTO `002` (email, fecha, aceptoavisolegal, estado, authkey)VALUES('%s', '$fecha', '$aceptoavisolegal', 'pendiente', '%s')",
        $_POST['email'],
        sha1($_POST['email']) 
    )
);
$rResult = mysql_query(
        sprintf(
            "INSERT INTO `013` (email, fecha, aceptoavisolegal, estado, authkey)VALUES('%s', '$fecha', '$aceptoavisolegal', 'pendiente', '%s')",
        $_POST['email'],
        sha1($_POST['email']) 
    )
);
    mail(
        $_POST['email'],
        'Confirmar solicitud',
        sprintf(
            'Confirmar solicitud de resultado:<br><br><a href="https://www.sanatusexo.com/recursos/an1c.php?key=%s ">Haga Click aquí para confirmar su solicitud gratuita</a><br><br>Si recibió este mensaje por error, simplemente ignórelo.<br><br>Su solicitud incluye una suscripción gratis a nuestra Newsletter que puede cancelarse en cualquier momento.<br><br>Si usted tiene alguna pregunta con respecto a este correo electrónico, contacte con nosotros en info@antonioferrandez.com.<br><br>Gracias y saludos cordiales,<br><br>Departamento de Administración',
            sha1($_POST['email'])
        ),
        'Content-type: text/html; charset=iso-8859-1' . "\r\n" .
    'MIME-Version: 1.0' . "\r\n" . 'From: Antonio Ferrandez<info@antonioferrandez.com>' . "\r\n" .
    'Reply-To: <info@antonioferrandez.com>' . "\r\n" .
    'X-Mailer: PHP/'
    );
    echo 'Gracias, por favor revise su email para confirmar la suscripción.';
    exit;
}
?>
