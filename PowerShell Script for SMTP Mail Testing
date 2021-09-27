$smtpServer = "email-smtp.us-east-1.amazonaws.com" 
$smtpPort = 587
$username = "<Access_id>"
$password = "<Passwords>"  
$from = "abc@example.com"
$to = "xyz@example.com"
$subject = "Testing emails with PowerShell Script"
$body = "This is a test e-mail sending with using PowerShell Script"

$smtp = new-object Net.Mail.SmtpClient($smtpServer, $smtpPort)
$smtp.EnableSsl = $true 

$smtp.Credentials = new-object Net.NetworkCredential($username, $password)
$msg = new-object Net.Mail.MailMessage
$msg.From = $from
$msg.To.Add($to)
$msg.Subject = $subject
$msg.Body = $body
$smtp.Send($msg)
