<br/>

<h3>This File has steps to run PHPIMageWorkshop on PHP versions less than 5.3</h3>
<br/>
	In your main file include the files in the following order

	require_once PATH_TO_PHP_IMAGE_WORKSHOP . '/PHPImageWorkshop/Exception/ImageWorkshopBaseException.php';
	require_once PATH_TO_PHP_IMAGE_WORKSHOP . '/PHPImageWorkshop/Exception/ImageWorkshopException.php';
	require_once PATH_TO_PHP_IMAGE_WORKSHOP . '/PHPImageWorkshop/Core/Exception/ImageWorkshopLayerException.php';
	require_once PATH_TO_PHP_IMAGE_WORKSHOP . '/PHPImageWorkshop/Core/Exception/ImageWorkshopLibException.php';
	require_once PATH_TO_PHP_IMAGE_WORKSHOP . '/PHPImageWorkshop/Core/ImageWorkshopLayer.php';
	require_once PATH_TO_PHP_IMAGE_WORKSHOP . '/PHPImageWorkshop/Core/ImageWorkshopLib.php';
	require_once PATH_TO_PHP_IMAGE_WORKSHOP . '/PHPImageWorkshop/ImageWorkshop.php';


1. Change <code>static::</code> to <code>self::</code> throughout all files

2. In the file: <code><b>Imageworkshop.php</b></code>

	Comment out all the below lines

		namespace PHPImageWorkshop;
		use PHPImageWorkshop\Core\ImageWorkshopLayer as ImageWorkshopLayer;
		use PHPImageWorkshop\Core\ImageWorkshopLib as ImageWorkshopLib;
		use PHPImageWorkshop\Exception\ImageWorkshopException as ImageWorkshopException;
	
3. In the file: <code><b>Exception\ImageWorkshopBaseException.php</b></code>

	Comment out the line 

	    namespace PHPImageWorkshop\Exception;
	
	AND 

	    Replace \Exception with Exception in the __construct declaration
	

4. In the file: <code><b>Exception\ImageWorkshopException.php</b></code>

	Comment out the lines 	

	    namespace PHPImageWorkshop\Exception;
	    use PHPImageWorkshop\Exception\ImageWorkshopBaseException as ImageWorkshopBaseException;

5. In the file: <code><b>Core\ImageWorkshopLib.php</b></code>

	Comment out the lines 	

    	namespace PHPImageWorkshop\Core;
    	use PHPImageWorkshop\Core\Exception\ImageWorkshopLibException as ImageWorkshopLibException;

6. In the file: <code><b>Core\ImageWorkshopLayer.php</b></code>

	Comment out the lines 	

    	namespace PHPImageWorkshop\Core;
    	use PHPImageWorkshop\ImageWorkshop as ImageWorkshop;
    	use PHPImageWorkshop\Core\ImageWorkshopLib as ImageWorkshopLib;
    	use PHPImageWorkshop\Core\Exception\ImageWorkshopLayerException as ImageWorkshopLayerException;

7. In the file: <code><b>Core\Exception\ImageWorkshopLayerException.php</b></code>

	Comment out the lines 	

    	namespace PHPImageWorkshop\Core\Exception;
    	use PHPImageWorkshop\Exception\ImageWorkshopBaseException as ImageWorkshopBaseException;


8. In the file: <code><b>Core\Exception\ImageWorkshopLibException.php</b></code>

	Comment out the lines 	

    	namespace PHPImageWorkshop\Core\Exception;
    	use PHPImageWorkshop\Exception\ImageWorkshopBaseException as ImageWorkshopBaseException;

9. Njoy :)
