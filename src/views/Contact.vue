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