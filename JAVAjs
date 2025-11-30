const firstname=document.getElementById("firstname");
const middleinit=document.getElementById("middleinit");
const lastname=document.getElementById("lastname");
const email=document.getElementById("email");
const ssn=document.getElementById("ssn");
const dob=document.getElementById("dob");
const addr1=document.getElementById("addr1");
const addr2=document.getElementById("addr2");
const city=document.getElementById("city");
const state=document.getElementById("state");
const zip=document.getElementById("zip");
const phone=document.getElementById("phone");
const work=document.getElementById("work");
const un=document.getElementById("un");
const pass=document.getElementById("pass");
const pass2=document.getElementById("pass2");


firstname.oninput=function(){
    this.value=this.value.replace(/[^A-Za-z-' ]/g,"");
};


lastname.oninput=function(){
    this.value=this.value.replace(/[^A-Za-z-' ]/g,"");
};


middleinit.oninput=function(){
    this.value=this.value.replace(/[^A-Za-z]/g,"").slice(0,1);
};


email.onblur=function(){
    const r=/^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    if(!r.test(this.value)) this.setCustomValidity("Invalid email format");
    else this.setCustomValidity("");
};


ssn.oninput=function(){
    let v=this.value.replace(/\D/g,"").slice(0,9);
    if(v.length>5) v=v.replace(/(\d{3})(\d{2})(\d{1,4})/,"$1-$2-$3");
    else if(v.length>3) v=v.replace(/(\d{3})(\d{1,2})/,"$1-$2");
    this.value=v;
};


zip.oninput=function(){
    this.value=this.value.replace(/\D/g,"").slice(0,5);
};


phone.oninput=function(){
    this.value=this.value.replace(/\D/g,"").slice(0,10);
};


work.oninput=function(){
    this.value=this.value.replace(/\D/g,"").slice(0,10);
};


dob.onblur=function(){
    const d=new Date(this.value);
    const now=new Date();
    const age=(now-d)/31557600000;
    if(age<0||age>120) this.setCustomValidity("Invalid DOB");
    else this.setCustomValidity("");
};


un.oninput=function(){
    const r=/^[A-Za-z][A-Za-z0-9_-]{4,19}$/;
    if(!r.test(this.value)) this.setCustomValidity("Invalid username");
    else this.setCustomValidity("");
};


function validatePassword(){
    if(pass.value===un.value){
        pass.setCustomValidity("Password cannot equal username");
        return;
    }
    const r=/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d).{8,}$/;
    if(!r.test(pass.value)){
        pass.setCustomValidity("Weak password");
        return;
    }
    pass.setCustomValidity("");
}


pass.oninput=validatePassword;


pass2.oninput=function(){
    if(pass2.value!==pass.value) pass2.setCustomValidity("Passwords do not match");
    else pass2.setCustomValidity("");
};




