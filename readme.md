# Codeigniter 3 Assessment


These assessments questions is designed to evaluate developer's understanding on the framework. To answer the questions, you may fork this repo and answer it in this codeigniter installation.

#### Question 1
Explain how to create a static page with the given uri `http://{domain}/page/about`.
Answer: http://myprestasi/highimpact/index

#### Question 2
From solution no 1, explain how to change the uri to `http://{domain}/about`.
Answer: Don't know

#### Question 3
Given that you have a database schema as below: 
```mysql 
  CREATE TABLE news (
        id int(11) NOT NULL AUTO_INCREMENT,
        title varchar(128) NOT NULL,
        slug varchar(128) NOT NULL,
        text text NOT NULL,
        PRIMARY KEY (id),
        KEY slug (slug)
);
```

Explain how would you query a record and display it to the user when visiting the uri `http://{domain}/news/{slug}` where slug is equivalent to the `slug` column in the table.

Answer: Don't know.

#### Question 4
How can you prevent sql injection when providing for the solution in question 3.
Answer: Don't know.


#### Question 5
Explain how to create a page where user can create a news entry into the database.
Answer: public function __construct()	{
  $this->load->database(); 
}

#### Question 6
Explain how can you validate input from user in question 5.
Answer: Don't know.

#### Question 7
Explain how can you save a user session when a user has logged in and how to retrieve the session.
Answer: $sess_array = array(
'id' => $row->Login_Id,
'username' => $row->Login_Name,
'postid'=> $row->Fk_Post_Id,
 );
$CI->session->set_userdata('logged_in', $sess_array);
then

$logged_in = $this->session->userdata('logged_in');
$createdby = $logged_in['id'];

#### Question 8
Show how can you prevent file upload with size not more than 2MB and only to accept `pdf` file.
Answer: function SubmitForm() {
                    var imgpath = document.getElementById("fileUpload").value;
                    if(imgpath=="")
                    {
                        document.getElementById("lblError").innerHTML = "No file was chosen before clicking on Upload button. Please chose a file first.";
                        return;
                    }

                    var allowedFiles = [".pdf"];
                    var fileUpload = document.getElementById("fileUpload");
                    var lblError = document.getElementById("lblError");
                    var regex = new RegExp("([a-zA-Z0-9\s_\\.\-:])+(" + allowedFiles.join('|') + ")$");
                    if (!regex.test(fileUpload.value.toLowerCase())) {
                        lblError.innerHTML = "Please upload files having extensions: <b>" + allowedFiles.join(', ') + "</b> only.";
                        return;
                    }
                    if (fileUpload.files[0].size > 2097152){
                        lblError.innerHTML = "File size is more than 2 MB.";
                        return;
                    }
                    lblError.innerHTML = "";
                    return;

                    lblError.innerHTML = "File Upload in Progress.......";
                    document.form.action = "upload_filedata.asp";
                    document.form.submit();

                } 

#### Question 9
Based on the schema in question 3, show how you write a migration class to create the table using codeigniter.
Answer: Don't know.

#### Question 10
What do you think of codeigniter compared to other PHP frameworks available e.g Laravel, Symfony, CakePHP
Answer: Robust and powerful by means of a well-designed toolkit, CodeIgniter is a prominent PHP framework. It is perfect for web applications development with advanced features.
