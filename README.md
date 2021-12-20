# contactforms
Working contact form

I am having issues with my contact form. This is the code and following it is the php

<form id="contact-form" action="contact.php" method="post">
                            <div class="input-group">
                                <input type="text" name="name" placeholder="Enter your name">
                                <div class="icon"><i class="fal fa-user"></i></div>
                            </div>
                            <div class="input-group mt-20">
                                <input type="email" name="email" placeholder="Enter your email">
                                <div class="icon"><i class="fal fa-envelope"></i></div>
                            </div>
                            <div class="input-group textarea-group mt-20">
                                <textarea name="message" id="message" cols="30" rows="10" placeholder="Enter your message"></textarea>
                                <div class="icon"><i class="fal fa-edit"></i></div>
                            </div>
                            <div class="input-group mt-20">
                                <button class="main-btn" type="submit">Submit Now</button>
                            </div>
                        </form>
                        
                        
                        
  <?php

    $name = $_POST['name'];
    $visitor_email = $_POST['email'];
    $message = $_POST['message'];
    
    
    $email_from = 'ifeanyianagor@gmail.com';
    
    $email_subject = "New Form Submission";
    
    $email_body = "User Name: $name. \n".
                    "User Email: $visitor_email.\n".
                           "User Message: $message.\n";
                        
                        
    $to = "2929concepts@gmail.com.com";
    
    $headers = "From: $email_from \r\n";
    
    $headers .= "Reply-To: $visitor_email \r\n";
    
    mail($to,$email_subject,$email_body,$headers);
    
    header("Location: contact.html");
?>
