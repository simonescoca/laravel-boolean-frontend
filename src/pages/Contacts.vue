<template>
    <div class="contact-information-navbar">

        <!-- Contact Information Section -->
        <div class="jumbotron">
            <h1>
                <!-- Title -->
                Contact Information
            </h1>
        </div>

        <!-- Navbar Buttons -->
        <nav>
            <ul>
                <div v-for="element in elements" class="contact-nav-button">
                    <li>
                        <a :href="element.link">{{ element.name }}</a>
                    </li>
                </div>
            </ul>
        </nav>

        <div class="side right-side">
            <div class="picture-wrapper">

            </div>
        </div>
    </div>

    <!-- Contact Form on Website -->
    <div class="contact-form">
        <div class="d-flex justify-content-center align-items-center">
            <h2>Contact us directly on the website!</h2>
        </div>


        <div class="row justify-content-center">
            <div class="col-lg-10 col-md-12">
                <div class="wrapper">
                    <div class="row justify-content-center">
                        <div class="col-lg-8 mb-5">
                            <div class="row">
                                <div class="col-md-4">
                                    <div class="dbox w-100 text-center">
                                        <div class="icon d-flex align-items-center justify-content-center">
                                            <svg xmlns="http://www.w3.org/2000/svg" height="1em"
                                                viewBox="0 0 384 512"><!-- Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                                <path
                                                    d="M215.7 499.2C267 435 384 279.4 384 192C384 86 298 0 192 0S0 86 0 192c0 87.4 117 243 168.3 307.2c12.3 15.3 35.1 15.3 47.4 0zM192 128a64 64 0 1 1 0 128 64 64 0 1 1 0-128z" />
                                            </svg>
                                        </div>
                                        <div class="text">
                                            <p><span>Address:</span> 198 West 21th Street, Suite 721 New York NY 10016</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-md-4">
                                    <div class="dbox w-100 text-center">
                                        <div class="icon d-flex align-items-center justify-content-center">
                                            <svg xmlns="http://www.w3.org/2000/svg" height="1em"
                                                viewBox="0 0 512 512"><!--Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                                <path
                                                    d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z" />
                                            </svg>
                                        </div>
                                        <div class="text">
                                            <p><span>Phone:</span> <a href="tel://1234567920">+ 1235 2355 98</a></p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-md-4">
                                    <div class="dbox w-100 text-center">
                                        <div class="icon d-flex align-items-center justify-content-center">
                                            <svg xmlns="http://www.w3.org/2000/svg" height="1em"
                                                viewBox="0 0 512 512"><!-- Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                                <path
                                                    d="M64 112c-8.8 0-16 7.2-16 16v22.1L220.5 291.7c20.7 17 50.4 17 71.1 0L464 150.1V128c0-8.8-7.2-16-16-16H64zM48 212.2V384c0 8.8 7.2 16 16 16H448c8.8 0 16-7.2 16-16V212.2L322 328.8c-38.4 31.5-93.7 31.5-132 0L48 212.2zM0 128C0 92.7 28.7 64 64 64H448c35.3 0 64 28.7 64 64V384c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V128z" />
                                            </svg>
                                        </div>
                                        <div class="text">
                                            <p><span>Email:</span> <a href="mailto:info@yoursite.com">info@yoursite.com</a>
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-lg-8">
                            <div class="contact-wrap">
                                <h3 class="mb-4 text-center">Get in touch with us</h3>
                                <div id="form-message-warning" class="mb-4 w-100 text-center"></div>
                                <div id="form-message-success" class="mb-4 w-100 text-center">
                                    Type here your message, and we'll reply to you as soon as we can!
                                </div>

                                <form method="POST" id="contactForm" name="contactForm" class="contactForm">
                                    <div class="row">
                                        <div class="col-md-12">
                                            <div class="form-group">
                                                <input type="text" class="form-control" name="name" id="name"
                                                    placeholder="Name">
                                            </div>
                                        </div>
                                        <div class="col-md-12">
                                            <div class="form-group">
                                                <input type="email" class="form-control" name="email" id="email"
                                                    placeholder="Email">
                                            </div>
                                        </div>
                                        <div class="col-md-12">
                                            <div class="form-group">
                                                <input type="text" class="form-control" name="subject" id="subject"
                                                    placeholder="Subject">
                                            </div>
                                        </div>
                                        <div class="col-md-12">
                                            <div class="form-group">
                                                <textarea name="message" class="form-control" id="message" cols="30"
                                                    rows="8" placeholder="Message"></textarea>
                                            </div>
                                        </div>
                                        <div class="col-md-12">
                                            <div class="form-group">
                                                <input type="submit" value="Send Message" class="btn btn-primary">
                                                <div class="submitting"></div>
                                            </div>
                                        </div>
                                    </div>

                                    <div class="form-check">
                                        <input class="form-check-input" type="checkbox" value="" id="flexCheckChecked"
                                            checked>
                                        <label class="form-check-label" for="flexCheckChecked">
                                            Do you want to subscribe to our newsletter as well?
                                        </label>
                                    </div>

                                </form>

                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    components: {},
    data() {
        return {
            elements,
        };
    },
};

const elements = [
    {
        name: "Contact",
        link: "/contact",
    },
    {
        name: "FAQ",
        link: "/faq",
    },
    {
        name: "Shipping",
        link: "/shipping",
    },
    {
        name: "Returns",
        link: "/returns",
    },
    {
        name: "Cookies",
        link: "/cookies",
    },
    {
        name: "Terms",
        link: "/terms",
    },
    {
        name: "Privacy",
        link: "/privacy",
    },

]
</script>

<style lang="scss">
@import "../styles/partials/variables.scss";

.contact-information-navbar {
    background-color: $background-color;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;

    .jumbotron {
        background-image: linear-gradient(rgba(200, 151, 151, 0.05), rgba(0, 0, 0, 0.80)), url(https://images.unsplash.com/photo-1597290282695-edc43d0e7129?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2075&q=80);
        width: 100%;
        overflow: hidden;
        height: 300px;
        background-position: 45% 25%;
        position: relative;

        h1 {
            font-size: 400;
            color: white;
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
        }
    }

    nav {
        ul {
            list-style: none;
            padding: 0px;
            display: flex;
            justify-content: space-evenly;
            flex-direction: row;

            li {
                margin: 20px;
            }

            .contact-nav-button {
                margin-bottom: 10px;

                a {
                    text-decoration: none;
                    color: #333;
                    font-weight: bold;
                    transition: color 0.3s ease;

                    &:hover {
                        color: $button-hover;
                    }
                }
            }
        }
    }

    .right-side {
        margin-top: 20px;
    }
}

.contact-form {
    background-color: $background-color;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);

    h2 {
        font-size: 24px;
        margin-bottom: 20px;
    }

    .dbox {
        .icon {
            font-size: 48px;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        &:hover {
            color: $button-hover;
            transform: scale(1.1);
            filter: brightness(0) saturate(100%) invert(83%) sepia(28%) saturate(480%) hue-rotate(355deg) brightness(99%) contrast(91%);
        }

        p {
            font-size: 14px;
            color: #777;
            text-align: center;
        }

        a {
            color: $text;
            text-decoration: none;
        }
    }

    .contact-wrap {
        .mb-4 {
            font-size: 16px;
        }

        .w-100 {
            text-align: center;
            font-size: 14px;
        }

        form {
            .form-control:focus{
                box-shadow: 0 0 0 0.25rem rgb(241, 208, 145);
            }

            .form-group {
                margin-bottom: 15px;

                input[type="text"],
                input[type="email"],
                textarea {
                    width: 100%;
                    padding: 10px;
                    border: 1px solid #ddd;
                    border-radius: 5px;
                    font-size: 14px;

                    &:focus {
                        outline: none;
                        border-color: $button;
                    }
                }

                input[type="submit"] {
                    background-color: $button;
                    color: #fff;
                    border: none;
                    border-radius: 5px;
                    padding: 10px 20px;
                    cursor: pointer;
                    font-size: 16px;
                    transition: background-color 0.3s ease;

                    &:hover {
                        background-color: $button-hover;
                    }
                }

                .submitting {
                    font-size: 14px;
                    color: $text;
                }
            }

            .form-check-input:checked {
                background-color: $button;
            }

            .form-check-label:hover {
                color: $button-hover;
            }
        }
    }
}
</style>
