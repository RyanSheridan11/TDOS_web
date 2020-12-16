<template>
    <div id="contact">
        <main>
            <div class="form-container">
                <form>

                    <label for="name">Full Name</label>
                    <input type="text" id="fname" name="fullname" placeholder="Enter your name*" />

                    <label for="email">Email Address</label>
                    <input type="text" id="email" name="emailaddress" placeholder="Enter your email address*" />

                    <label for="subject">Subject</label>
                    <input type="text" id="subject" name="subject" placeholder="Subject*" />

                    <label for="message">Message</label>
                    <textarea id="message" name="Message" placeholder="Enter your message here*" style="height:200px"></textarea>

                    <input type="submit" value="Submit" />
                </form>
            </div>
        </main>
    </div>
</template>

<style>
    input[type=text], select, textarea {
        width: 100%;
        padding: 12px;
        border: 2px solid #1C3334;
        border-radius:4px;
        box-sizing:border-box;
        margin-top:6px;
        margin-bottom:16px;
        resize:vertical;
    }

    input[type=submit]{
        background-color:#DA7B93;
        color:white;
        padding:12px 20px;
        border:none;
        border-radius:4px;
        cursor:pointer;
    }

    input[type=submit]:hover{
            background-color:#2E151B;
    }

.form-container{
    border-radius:5px;
    background-color:none;
    padding:20px;
    margin:20px;
}
</style>