<script></script>

<nav>
    <div class="navbar">
        <div class="container nav-container">
            <input class="checkbox" type="checkbox" name="" id="" />
            <div class="hamburger-lines">
                <span class="line line1" />
                <span class="line line2" />
                <span class="line line3" />
            </div>
            <div class="logo">
                <h1><a href="/">Navbar</a></h1>
            </div>
            <div class="menu-items">
                <li><a href="/">Home</a></li>
                <li><a href="/">about</a></li>
                <li><a href="/">blogs</a></li>
                <li><a href="/">portfolio</a></li>
                <li><a href="/">contact</a></li>
            </div>
        </div>
    </div>
</nav>

<style>
    .checkbox {
        display: none;
    }
    h1 a {
        text-decoration: none;
        color: #000;
    }
    .navbar {
        height: 12vh;
        width: 100%;
    }
    .container {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        height: 100%;
    }
    .logo {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: start;
        width: 100%;
        height: 100%;
        padding: 0 0 0 1rem;
    }
    .menu-items {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        width: 60%;
        height: 100%;
        list-style: none;
    }
    .menu-items li {
        display: inline-block;
    }
    .menu-items li a {
        text-decoration: none;
        color: black;
        width: 100%;
        font-size: 1.5rem;
        padding: 0 0 0 1rem;
    }
    @media screen and (max-width: 600px) {
        .container {
            max-width: 1050px;
            width: 90%;
            margin: auto;
            z-index: 100;
        }

        .navbar {
            width: 100%;
            box-shadow: 0 1px 4px rgb(146 161 176 / 15%);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 62px;
        }

        .navbar .menu-items {
            display: flex;
        }

        .navbar .nav-container li {
            list-style: none;
        }

        .navbar .nav-container a {
            text-decoration: none;
            color: #0e2431;
            font-weight: 500;
            font-size: 1.2rem;
            padding: 0.7rem;
        }

        .navbar .nav-container a:hover {
            font-weight: bolder;
        }

        .nav-container {
            display: block;
            position: relative;
            height: 60px;
        }

        .nav-container .checkbox {
            position: absolute;
            display: block;
            height: 32px;
            width: 32px;
            top: 20px;
            left: 20px;
            z-index: 5;
            opacity: 0;
            cursor: pointer;
            z-index: 150;
        }

        .nav-container .hamburger-lines {
            display: block;
            height: 26px;
            width: 32px;
            position: absolute;
            top: 17px;
            left: 20px;
            z-index: 2;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .nav-container .hamburger-lines .line {
            display: block;
            height: 4px;
            width: 100%;
            border-radius: 10px;
            background: #0e2431;
        }

        .nav-container .hamburger-lines .line1 {
            transform-origin: 0% 0%;
            transition: transform 0.4s ease-in-out;
        }

        .nav-container .hamburger-lines .line2 {
            transition: transform 0.2s ease-in-out;
        }

        .nav-container .hamburger-lines .line3 {
            transform-origin: 0% 100%;
            transition: transform 0.4s ease-in-out;
        }

        .navbar .menu-items li {
            margin-bottom: 1.2rem;
            font-size: 1.5rem;
            font-weight: 500;
            z-index: 100;
        }

        .logo {
            position: absolute;
            top: 5px;
            right: 15px;
            font-size: 1.2rem;
            color: #0e2431;
        }

        .nav-container input[type="checkbox"]:checked ~ .menu-items {
            transform: translateX(0);
        }

        .nav-container
            input[type="checkbox"]:checked
            ~ .hamburger-lines
            .line1 {
            transform: rotate(45deg);
        }

        .nav-container
            input[type="checkbox"]:checked
            ~ .hamburger-lines
            .line2 {
            transform: scaleY(0);
        }

        .nav-container
            input[type="checkbox"]:checked
            ~ .hamburger-lines
            .line3 {
            transform: rotate(-45deg);
        }

        .nav-container input[type="checkbox"]:checked ~ .logo {
            display: none;
        }
        .navbar .menu-items {
            padding-top: 120px;
            background-color: white;
            height: 100vh;
            width: 100vw;
            transform: translate(-150%);
            display: flex;
            flex-direction: column;
            margin-left: -40px;
            padding-left: -40px;
            transition: transform 0.5s ease-in-out;
            text-align: center;
            z-index: 100;
        }

        h1 a {
            display: none;
        }
    }
</style>
