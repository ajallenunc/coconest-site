---
layout: page
title: Contact Me
permalink: /pages/contact-me
---

{::nomarkdown}
<div id="contact">
    <h2>Get in Touch</h2>
    <p>Have any questions or recommendations to improve CoCoNest? Fill out the form below and I'll try to get back to you as soon as possible.</p>
    <div id="contact-form">
        <form action="https://formspree.io/f/xnqekkjk" method="POST" name="sentMessage" id="contactForm" novalidate>
            <input type="hidden" name="_subject" value="Contact request from personal website" />
            <div class="row control-group">
                <div class="form-group col-xs-12 floating-label-form-group controls">
                    <label>Name</label>
                    <input type="text" class="form-control" placeholder="Name" id="name" name="name" required data-validation-required-message="Please enter your name.">
                    <p class="help-block text-danger"></p>
                </div>
            </div>
            <div class="row control-group">
                <div class="form-group col-xs-12 floating-label-form-group controls">
                    <label>Email Address</label>
                    <input type="email" class="form-control" placeholder="Email Address" id="email" name="_replyto" required data-validation-required-message="Please enter your email address.">
                    <p class="help-block text-danger"></p>
                </div>
            </div>
            <div class="row control-group">
                <div class="form-group col-xs-12 floating-label-form-group controls">
                    <label>Phone Number</label>
                    <input type="tel" class="form-control" placeholder="Phone Number" id="phone" name="phone" required data-validation-required-message="Please enter your phone number.">
                    <p class="help-block text-danger"></p>
                </div>
            </div>
            <div class="row control-group">
                <div class="form-group col-xs-12 floating-label-form-group controls">
                    <label>Message</label>
                    <textarea rows="5" class="form-control" placeholder="Message" id="message" name="message" required data-validation-required-message="Please enter a message."></textarea>
                    <p class="help-block text-danger"></p>
                </div>
            </div>
            <br>
            <div id="success"></div>
            <div class="row">
                <div class="form-group col-xs-12">
                    <button type="submit" class="btn btn-default">Send</button>
                </div>
            </div>
        </form>
    </div>
</div>
{:/nomarkdown}
Test
