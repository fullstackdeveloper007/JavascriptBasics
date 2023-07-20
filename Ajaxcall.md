$.ajax({
            url: "/api/Authentication/MethodName",
            type: 'POST',
            contentType: "application/json; charset=utf-8",
            data: JSON.stringify({
                UserName: loginId
            }),
            dataType: "json",
            success: function (res) {
                if (res === false) {
                    $('input[type=submit]').focus();
                    document.getElementById("backdrop").style.display = "flex";
                     
                } else {
                    document.getElementById("backdrop").style.display = "none";
                }
            }, error: function (xhr, status, error) {                
                
            }
        });


 ## 1. The below is fetch() merhod no jquery library will be required as above. It is build in Js libarary function.  
const loginId = "your_login_id"; // Replace this with the actual loginId

// Data to be sent in the request body
const requestData = {
  UserName: loginId
};

fetch("/api/Authentication/CheckLoginSession", {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json; charset=utf-8'
  },
  body: JSON.stringify(requestData)
})
  .then(response => response.json())
  .then(res => {
    if (res === false) {
      $('input[type=submit]').focus();
      document.getElementById("backdrop").style.display = "flex";
    } else {
      document.getElementById("backdrop").style.display = "none";
    }
  })
  .catch(error => {
    // Handle errors
    console.error('Error fetching data:', error);
  });
 






