## Ajax Call
<pre class="notranslate">
<code>	
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

</code></pre>	

 ### The below is js fetch() method and no jquery or any other library will be required for this. It is build in Js libarary function.  

 <pre class="notranslate">
<code>
const loginId = "your_login_id"; // Replace this with the actual loginId

// Data to be sent in the request body
const requestData = {
  UserName: loginId
};

fetch("/api/Authentication/MethodName", {
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
 </code></pre>	






