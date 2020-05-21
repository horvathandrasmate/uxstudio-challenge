<template>
  <div id="twitter"></div>
</template>

<script>
$.ajax({
            url: "https://guamanpj.eu/twitter-api",
            method: "POST", //First change type to method here

            data: {
                method:"isVip",
                value:"asd"
            },
            success: function(response) {
                console.log(response);
            },
            error: function() {
                alert("error");
            }

        });
</script>
<style></style>
