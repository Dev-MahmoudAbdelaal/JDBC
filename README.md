<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
<h1> JDBC Overview</h1>
<p>
    JDBC (Java Database Connectivity) is a Java API for connecting and executing queries on databases.
</p>

<!-- Point 1: Import JDBC packages -->
<h2>1. Import JDBC Packages</h2>
<p>
    To use JDBC, you need to import the necessary packages:
<pre><code>
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;
import java.sql.Statement;
import java.sql.ResultSet;
        </code></pre>
</p>

<!-- Point 2: Load and Register JDBC Driver -->
<h2>2. Load and Register JDBC Driver</h2>
<p>
    Before connecting to a database, you need to load and register the JDBC driver for your database.
    For example, if you're using MySQL:
<pre><code>
Class.forName("com.mysql.cj.jdbc.Driver");
        </code></pre>
</p>

<!-- Point 3: Establish Connection -->
<h2>3. Establish Connection</h2>
<p>
    Use the DriverManager class to establish a connection to the database. The connection URL typically consists of the following parts:
<ul>
    <li><strong>jdbc:</strong> The protocol for JDBC connections.</li>
    <li><strong>subprotocol:</strong> The database vendor-specific subprotocol.</li>
    <li><strong>hostname:</strong> The hostname or IP address of the database server.</li>
    <li><strong>port:</strong> The port number on which the database server is listening (optional).</li>
    <li><strong>database:</strong> The name of the specific database you want to connect to.</li>
</ul>
For example, to connect to a MySQL database running locally on the default port:
<pre><code>
Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/mydatabase", "username", "password");
        </code></pre>
Here, "jdbc:mysql://" specifies the MySQL subprotocol, "localhost" is the hostname, "3306" is the default MySQL port, and "mydatabase" is the name of the database.
</p>

<!-- Point 4: Create Statement -->
<h2>4. Create Statement</h2>
<p>
    Once the connection is established, you can create a Statement object for executing SQL queries:
<pre><code>
Statement statement = connection.createStatement();
        </code></pre>
</p>

<!-- Point 5: Execute Queries -->
<h2>5. Execute Queries</h2>
<p>
    You can execute SQL queries using the Statement object:
<pre><code>
ResultSet resultSet = statement.executeQuery("SELECT * FROM my_table");
        </code></pre>
</p>

<!-- Point 6: Process Results -->
<h2>6. Process Results</h2>
<p>
    You can iterate over the ResultSet to retrieve and process the query results:
<pre><code>
while (resultSet.next()) {
    // Process each row
}
        </code></pre>
</p>

<!-- Point 7: Close Resources -->
<h2>7. Close Resources</h2>
<p>
    It's important to close the ResultSet, Statement, and Connection objects after you're done using them:
<pre><code>
resultSet.close();
statement.close();
connection.close();
        </code></pre>
</p>
<p>
    Discover the perfect JDBC playlist for seamless learning and mastering database connectivity in Java! 
    <a href="https://www.youtube.com/playlist?list=PLEAQNNR8IlB4R7NfqBY1frapYo97L6fOQ">
        <img src="https://img.shields.io/badge/YouTube-Playlist-red" alt="JDBC Playlist" style="vertical-align: middle">
    </a>
</p>
</body>
</html>
