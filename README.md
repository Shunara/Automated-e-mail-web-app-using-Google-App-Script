https://script.google.com/a/macros/aluno.ifce.edu.br/s/AKfycbwXIGr5KyzpY8dt3TCOnKxbSWmdZKGChZg2umpe-jzDj-6wwAbvUG5nr9ijlbsoE3U/exec
# YOU DON'T HAVE TO BE LOGGED IN ANY E-MAIL ACCOUNT TO USE IT. 

# GOOGLE APP SCRIPT
function doGet() {
  //Return the HTML PAGE available in: https://script.google.com/a/macros/aluno.ifce.edu.br/s/AKfycbwXIGr5KyzpY8dt3TCOnKxbSWmdZKGChZg2umpe-jzDj-6wwAbvUG5nr9ijlbsoE3U/exec
  return HtmlService.createHtmlOutputFromFile("Index");
}

function e_mail(email,x,w,y,z){
  //Separating the e-mails:
  
  var emails = new Array;
  emails = email.split(",");

  for(i=0;i<emails.length;i++){
  GmailApp.sendEmail(emails[i],"Automated e-mail web app using Google App Script","",
  //E-mail message un HTML and CSS format 
  { htmlBody: "<html>"+
  "<head>"+
  "<style>"+
  "p{text-align:"+w+";color:"+y+";font-size:"+z+";}"+
  "</style>"+
  "</head>"+
  "<body>"+
  "<p>"+x+"</p><p>My name's Leonardo and I sent you this personalized e-mail using an online automated e-mail sender made in Google App Script. You should check it out! Here's the source code: https://github.com/Shunara/Automated-e-mail-web-app-using-Google-App-Script.</p>"+
  "</body>"});
  }

  return "Your message was sent to this(these) e-mail(s):"+"\n"+emails;
}

# ===== HTML/CSS/JAVASCRIPT ===
