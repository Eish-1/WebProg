# **Experiment No. 1**

**Problem Statement:**

Create a web page that covers your CV using various HTML tags (ul, ol, table etc.).

**Source code :**

<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My CV</title>
</head>
<body style="font-family: Arial, sans-serif; background-color: #f4f4f4; margin: 0; padding: 20px;">

    <h1 style="text-align: center; color: #333;">CV</h1>
    <img style="width: 100px;
    height: 100px;
    display: block;
    margin: 0 auto;" src="profile_pic.jpg" alt="profile_pic">

    <h2 style="text-align: center;">Personal Information</h2>
    <table border="1" align="center" cellpadding="7">
        <tr>
            <th >Full Name</th>
            <td >Eish Chandeal</td>
        </tr>
        <tr>
            <th >Email</th>
            <td >eishchandeal25@gmail.com</td>
        </tr>
        <tr>
            <th >Phone</th>
            <td >+91 7065191512</td>
        </tr>
        <tr>
            <th >Address</th>
            <td >Laxmi Bai Nagar New Delhi</td>
        </tr>
    </table>

    <h2 style="text-align: center;">Education</h2>
    <table border="1" align="center" cellpadding="7">
        <tr>
            <th >Degree</th>
            <th >Details</th>
        </tr>
        <tr>
            <td >10th Percentage</td>
            <td >74.5%</td>
        </tr>
        <tr>
            <td >12th Percentage</td>
            <td >88%</td>
        </tr>
        <tr>
            <td >JEE Percentile</td>
            <td >84%</td>
        </tr>
        <tr>
            <td >School Name</td>
            <td >D.T.E.A Laxmi Bai Nagar</td>
        </tr>
        <tr>
            <td >Currently Pursuing Degree</td>
            <td >B.Tech:AI and DS</td>
        </tr>
        <tr>
            <td >College Name</td>
            <td >Vivekananda Institute of Professional Studies - TC</td>
        </tr>
    </table>

    <h2 style="text-align: center;">Projects</h2>
    <ol style="margin-left: 20px;">
        <li>
            <strong>Project: E-Commerce Web Application</strong>
            <ul>
                <li>Developed a full-stack e-commerce platform using React for the frontend and Node.js with MongoDB for the backend.</li>
                <li>Implemented user authentication, product search, and a shopping cart system.</li>
                <li>Enhanced performance by integrating lazy loading and optimizing API calls, resulting in a 15% reduction in load times.</li>
            </ul>
        </li>
        <br>
        <li>
            <strong>Project: Task Management Application</strong>
            <ul>
                <li>Built a task management tool using React, allowing users to create, edit, and delete tasks.</li>
                <li>Integrated Node.js with a MongoDB database for backend functionality and real-time task synchronization.</li>
                <li>Added dynamic filtering and task prioritization features, improving user productivity by 25%.</li>
            </ul>
        </li>
    </ol>


    <h2 style="text-align: center;">Skills</h2>
    <ul style="margin-left: 20px;">
        <li>Programming Languages: JavaScript, Python, C++</li>
        <li>Web Development: HTML, CSS, React, Node.js</li>
        <li>Databases: MongoDB, MySQL</li>
    </ul>

    <h2 style="text-align: center;">Certifications</h2>
    <ol style="margin-left: 20px;">
        <li>Certified JavaScript Developer (2022)</li>
        <li>ReactJS Certification (2023)</li>
    </ol>

    <h2 style="text-align: center;">Languages</h2>
    <ul style="margin-left: 20px;">
        <li>Hindi (Fluent)</li>
        <li>English (Intermediate)</li>
    </ul>

    <h2 style="text-align: center;">Hobbies</h2>
    <ul style="margin-left: 20px;">
        <li>Reading tech blogs</li>
        <li>Playing chess</li>
        <li>Coding side projects</li>
    </ul>

</body>
</html>
