---
layout: page
title: Contact Me
permalink: /pages/contact-me
---

<head>
    <!-- Include only necessary Bootstrap CSS for the form -->
    <style>
        #custom-contact-form .floating-label-form-group {
            position: relative;
            margin-bottom: 1.5em;
        }

        #custom-contact-form .floating-label-form-group input,
        #custom-contact-form .floating-label-form-group textarea {
            z-index: 1;
            position: relative;
            padding-right: 0;
            padding-left: 0;
            border-radius: 0;
            font-size: 1.5em;
            background: none;
            border: none;
            border-bottom: 1px solid #ddd;
            box-shadow: none !important;
            resize: none;
        }

        #custom-contact-form .floating-label-form-group label {
            position: absolute;
            top: 0;
            left: 0;
            display: block;
            width: 100%;
            margin: 0;
            padding: 7px 0;
            pointer-events: none;
            border: 1px solid transparent;
            border-radius: 3px;
            transition: all 0.2s ease;
        }

        #custom-contact-form .floating-label-form-group input:focus ~ label,
        #custom-contact-form .floating-label-form-group input:not(:focus):valid ~ label,
        #custom-contact-form .floating-label-form-group textarea:focus ~ label,
        #custom-contact-form .floating-label-form-group textarea:not(:focus):valid ~ label {
            top: -1.5em;
            font-size: 0.85em;
            color: #333;
        }

        #custom-contact-form .floating-label-form-group input:focus,
        #custom-contact-form .floating-label-form-group textarea:focus {
            border-bottom: 1px solid #555;
            outline: none;
        }

        #custom-contact-form .form-group {
            margin-bottom: 15px;
        }

        #custom-contact-form .btn {
            display: inline-block;
            padding: 6px 12px;
            margin-bottom: 0;
            font-size: 14px;
            font-weight: normal;
            line-height: 1.42857143;
            text-align: center;
            white-space: nowrap;
            vertical-align: middle;
            -ms-touch-action: manipulation;
                touch-action: manipulation;
            cursor: pointer;
            background-image: none;
            border: 1px solid transparent;
            border-radius: 4px;
            user-select: none;
        }

        #custom-contact-form .btn-default {
            color: #333;
            background-color: #fff;
            border-color: #ccc;
        }
    </style>
</head>

<body>
    <div id="contact">
        <h2>Have any questions or recommendations for improving CoCoNest? Leave me a message below and I'll try to get back to you shortly.</h2>
        <div id="contact-form">
            <form id="custom-contact-form" action="https://formspree.io/f/xnqekkjk" method="POST" name="sentMessage" novalidate>
                <input type="hidden" name="_subject" value="Contact request from personal website" />
                <div class="row control-group">
                    <div class="form-group col-xs-12 floating-label-form-group controls">
                        <input type="text" class="form-control" placeholder="Name" id="name" name="name" required data-validation-required-message="Please enter your name.">
                        <p class="help-block text-danger"></p>
                    </div>
                </div>
                <div class="row control-group">
                    <div class="form-group col-xs-12 floating-label-form-group controls">
                        <input type="email" class="form-control" placeholder="Email Address" id="email" name="_replyto" required data-validation-required-message="Please enter your email address.">
                        <p class="help-block text-danger"></p>
                    </div>
                </div>
                <div class="row control-group">
                    <div class="form-group col-xs-12 floating-label-form-group controls">
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

    <!-- Include jQuery and Bootstrap JavaScript -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>

    <!-- Custom JavaScript for floating labels -->
    <script>
        $(function() {
            $("body").on("input propertychange", ".floating-label-form-group", function(e) {
                $(this).toggleClass("floating-label-form-group-with-value", !!$(e.target).val());
            }).on("focus", ".floating-label-form-group", function() {
                $(this).addClass("floating-label-form-group-with-focus");
            }).on("blur", ".floating-label-form-group", function() {
                $(this).removeClass("floating-label-form-group-with-focus");
            });
        });
    </script>
</body>

