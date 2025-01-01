<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inideed with search</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f8f9fa;
        }

        
        .header {
            background-color: #007BFF;
            color: rgb(50, 48, 48);
            padding: 20px;
            text-align: center;
        }
        .search-bar {
            margin-bottom: 20px;
            padding: 10px;
            width: 100%;
            max-width: 500px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .navbar {
            display: flex;
            justify-content: center;
            background-color: #343a40;
            padding: 10px 0;
        }

        .navbar a {
            color: rgb(212, 25, 25);
            text-decoration: none;
            padding: 10px 20px;
        }

        .navbar a:hover {
            background-color: #3578ba;
            border-radius: 5px;
        }

        .content {
            padding: 20px;
        }

        .job {
            background: rgb(65, 197, 120);
            margin: 10px auto;
            padding: 20px;
            max-width: 600px;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .job h3 {
            margin: 0 0 10px;
            color: #007BFF;
        }

        .job p {
            margin: 0 0 10px;
            color: #555;
        }

        .job button {
            padding: 10px 15px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .job button:hover {
            background-color: #0056b3;
        }

        .footer {
            text-align: center;
            padding: 10px;
            background-color: #343a40;
            color: white;
            margin-top: 20px;
        }
    </style>
</head>
<body>
<div class="header">
    <h1>Inideed</h1>
    <p>Your gateway to amazing opportunities</p>
</div>
<!-- Navigation Bar -->
<div class="navbar">
    <a href="#">Home</a>
    <a href="#">Jobs</a>
    <a href="#">Post a Job</a>
    <a href="#">Contact Us</a>
    <a href="#"> Help center</a>
    <a href="#">company reviews</a>
    <a href="#">creat your CV</a>

</div>
<div class="content">
    <input type="text" id="search" class="search-bar" placeholder="Search for jobs..." onkeyup="searchJobs()">

    <div class="job">
        <h3>Frontend Developer</h3>
        <p>Company: Tech Solutions</p>
        <p>Location: New York, NY</p>
        <p>Experience: 2+ years</p>
        <button>Apply Now</button>
    </div>

    <div class="job">
        <h3>Backend Developer</h3>
        <p>Company: Innovatech</p>
        <p>Location: San Francisco, CA</p>
        <p>Experience: 3+ years</p>
        <button>Apply Now</button>
    </div>

    <div class="job">
        <h3>Data Scientist</h3>
        <p>Company: DataWorks</p>
        <p>Location: Austin, TX</p>
        <p>Experience: 4+ years</p>
        <button>Apply Now</button>
    </div>
    <div class="job">
        <h3>Data analyst</Data></h3>
        <p>Company: web scraper</p>
        <p>Location: pune,india</p>
        <p>Experience: 0-1 years</p>
        <button>Apply Now</button>
    </div>
    <div class="job">
        <h3>python Developer</h3>
        <p>Company: Developer</p>
        <p>Location: Mumbai,In</p>
        <p>Experience: 1 year</p>
        <button>Apply Now</button>
    </div>
    <script>
        function searchJobs() {
            var input, filter, jobList, jobs, h3, i, txtValue;
            input = document.getElementById('search');
            filter = input.value.toUpperCase();
            jobList = document.getElementById('job-list');
            jobs = jobList.getElementsByTagName('li');
    
            for (i = 0; i < jobs.length; i++) {
                h3 = jobs[i].getElementsByTagName('h3')[0];
                if (h3) {
                    txtValue = h3.textContent || h3.innerText;
                    if (txtValue.toUpperCase().indexOf(filter) > -1) {
                        jobs[i].style.display = "";
                    } else {
                        jobs[i].style.display = "none";
                    }
                }
            }
        }
    </script>
</div>
<div class="footer">
    <p>&copy; 2025 Job Portal. All rights reserved.</p>
</div>

</body>
</html>

