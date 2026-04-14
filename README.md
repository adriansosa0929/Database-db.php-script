<?php
header('Access-Control-Allow-Origin: *');
header('Content-Type: application/json');
require_once 'db.php';
$data = json_decode(file_get_contents('php://input'), true);
$db = getDB();
$stmt = $db->prepare("SELECT * FROM users WHERE username = ?");
$stmt->execute([$data['id']]);
$user = $stmt->fetch();
if ($user) {
echo json_encode(array('success' => true, 'tier' => 'Standard'));
} else {
echo json_encode(array('success' => false, 'error' => 'Invalid login'));
}
?>
