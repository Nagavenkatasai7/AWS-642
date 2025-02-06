Hello Sabiha Salma, 

I hope you are having a wonderful day. 

Coming to the website, as per the instructions from the professors, I created 3 HTML pages. They are 

index.html that showcases myself and my previous works, The second one is the cs_department_info_page.html page, where I display a short info on the CS Department and the various degrees in the CS Department and the mandatory courses of each course that should be completed to meet the requirements of getting a degree. The third is the student_survey_form.html, where we collect the student's basic info like name, email, address, date, etc. Now I will explain everything I did on each website.



Part 1:

index.html

In this HTML page, we took the template from W3Schools (https://www.w3schools.com/w3css/w3css_templates.asp) and edited the required components on the page. In the navbar, I had two more components added in the given template, which redirect to the cs_department_info_page.html. The other component is the student_survey_form.html.I also added some cool icons to both of the components to make them look nice. As instructed by the professor, I added my profile picture to the web page using the .image tag and then described myself using the .paragraph tag. Then I show cased my skills using a bar graph. Then I posted a few of my research publications I worked on during my undergrad.



Part 2:

cs_department_info_page.html



First I will describe cs_department_info_page. This is where I used the HTML, CSS Bootstrap framework.

I added a navbar that can access 3 modules of the website: Home, Courses, and Requirements, and at the end, I added a search bar.

Then the body is divided into 3 parts; in the first part, we have described a little summary about the college. And added a small image that sneak peeks the campus. Also, we have a button to visit campus that will redirect us to the GMU Computer Science department web page.

Now the second part showcases different types of master's degree programs available in the computer science department.

The third part shows what the criteria and the required courses are that a student should complete in that degree to obtain a master's degree.

Below it is the survey form.

And finally the footer, where I added all the social media links of GMU to make the website look more dynamic.



student_survey_form.html 



Now the survey form. The welcome section is designed based on the instructions given by the professor.

First we have the username, then his full name, surname, email, URL, address, date, checkboxes that ask students what they like most on campus?, and then the radio buttons for the high school graduation month of the student. And the user can add any comments he/she likes. Then the user can submit the form.

But here is where the magic happens. The form will check whether all the required criteria are filled in or not. If any of the mandatory criteria are missing, the form will not submit the response.

So all the mandatory columns are pointed with a red * sign.

And once the user fills in his information, if he/she wants to add another response, they don't have to fill in all the details again because we enabled the option auto fill, which will automatically fill in the previous details to make the user's life easy.



AWS S3:

1. First, I created a bucket with the name class-website.

2. After that, I uploaded the website folder into the bucket.

3. Now I made a few changes in the permission section to make my website publicly accessible.

4. I first enabled static website hosting in my properties; there I gave my index.html file name and then saved my changes.

5. Then in permissions, I disabled block public access to make the website accessible to the public.

6. Now again in permission I made changes in the object ownership where I enabled access-controlled list (ACL).

7. Then selected all files in the folder and went to ACTIONS and selected make public using ACL.

8. Now the website is available for public access.

URL: https://class-website.s3.us-east-1.amazonaws.com/HA-642/classWebsite.html



AWS EC2 Instance

1. First I created an instance in EC2. With the name classwebsite1. The application OS is Ubuntu, and the AMI was the Amazon Linux 2023 AMI, which is free tier eligible. Instance type as t2.micro 1 vCPU, 1 GiB memory. Create a new key pair class website 1. Then I allowed HTTP traffic in networking settings to host my website. And launched the website.

2. Now as the next step, I connected to the SSH client through my terminal.

3. First I have checked the permission to my PEM file (chmod 400 /Users/nagavenkatasaichennu/Desktop/AWS/classwebsite1.pem).

4. Then I entered the file path to my PEM file and the folder that consists of my code (ssh -i "classwebsite1.pem" ubuntu@ec2-44-208-32-239.compute-1.amazonaws.com). Then I was entered into the Ubuntu OS.

5. Now I installed the required package, like Apache (sudo apt install apache2 -y).

6. To add my file, I felt the best way is to clone the files from my git repository (sudo git clone https://github.com/Nagavenkatasai7/AWS-642). So I cloned the website files from the GitHub repository.

7. Now I configured the Apache to change the ownership (sudo chown -R www-data:www-data /var/www/html/). And restart the Apache. (sudo systemctl restart apache2)

8. I made sure all the permissions and configurations are correct (sudo nano /etc/apache2/sites-available/000-default.conf).

9. Then I have disabled the Apache default webpage (sudo rm /var/www/html/index.html). 

10. And now I was able to access my website.






