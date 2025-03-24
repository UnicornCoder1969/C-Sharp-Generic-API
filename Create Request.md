Task 2 

Version Log

Asset Log

Actual Code

Test Log

# Get Data:
```

string connectionString = "Data Source = (LocalDB)\\MSSQLLocalDB; AttachDbFilename = file path ; Integrated Security = True; Connect Timeout = 30"; 
SqlConnection sqlConnection = new SqlConnection(connectionString);
 
SqlCommand command = new SqlCommand("command name", sqlConnection); 
command.CommandType = CommandType.StoredProcedure;
 
command.Parameters.AddWithValue("@parameter", variable);
 
SqlDataAdapter sd = new SqlDataAdapter(cmd);
DataTable name = new DataTable()
 
sqlConnection.Open(); 
sd.Fill(datatable name); 
sqlConnection.Close();
 
foreach (DataRow dr in datatablename.Rows) 
{
            datatype variablename = (cast data type)(dr["column name"]); - regular get from datatable
            string variable = dr["column"] != DBNull.Value ? (string)(dr["column"]) : "N/A"; - conditional get from datatable (gets data, if column for that row is blank, sets it as "N/A")
            do the print to text box and stuff here
}
 ```

# GET Stored Procedure:
```

Create procedure [dbo].[procedure name]
 
( 
@param1 type, 
@param2 type 
)
 
as 
begin 
Select * from TABLE where condition
end
```

# SET Data C# Code:
```

string connectionString = "Data Source = (LocalDB)\\MSSQLLocalDB; AttachDbFilename = file path ; Integrated Security = True; Connect Timeout = 30"; 
SqlConnection sqlConnection = new SqlConnection(connectionString);
 
SqlCommand command = new SqlCommand("command name", sqlConnection); 
command.CommandType = CommandType.StoredProcedure;
 
command.Parameters.AddWithValue("@parameter", variable);
 
sqlConnection.Open(); 
command.ExecuteNonQuery(); 
sqlConnection.Close();
 
 ```

# SET Data Stored Procedure:
```

Create procedure [dbo].[procedure name]
 
( 
@param1 type, 
@param2 type 
)
 
as 
begin 
Insert into TABLE values @param1, @param2 (where goes here if you want it)
end
```

# TO get data
```

using (SqlConnection connection = new SqlConnection(_connectionString))
{
    connection.Open();

    using (SqlCommand command = new SqlCommand(SQLquery, connection))
    {
        using (SqlDataReader reader = command.ExecuteReader())
        {
            while (reader.Read())
            {
                users.Add(
                    new User(
                        int.Parse(reader["UserID"].ToString()), 
                        reader["Username"].ToString(), 
                        reader["Password"].ToString()
                    )
                );
            }
        }
    }
}
```

# TO set data
```

string query = "INSERT INTO Users (Username, Password) VALUES (@Username, @Password)";

// Insert the new user into the database using SQL command
using (var connection = new SqlConnection(_connectionString))
using (var command = new SqlCommand(query, connection))
{
    connection.Open(); 

    command.Parameters.AddWithValue("@Username", txtUsername.Text);
    command.Parameters.AddWithValue("@Password", txtPassword.Text);

    int result = command.ExecuteNonQuery();

   
    if (result > 0)
    {
        users.Add(user); 
        MessageBox.Show("Successfully Created Account", "Health Advice Group - Sign Up", MessageBoxButtons.OK, MessageBoxIcon.Information);
    }
```

# API Get data

            string key = "";
            string url = $"https://api.openweathermap.org/data/2.5/forecast?lat={lat}&lon={lon}&appid={key}&mode=json&units=metric";

            // Create an HttpClient instance to make the GET request
            using (HttpClient client = new HttpClient())
            {
                HttpResponseMessage response = client.GetAsync(url).Result;  // Using .Result to block and wait for the result

                if (!response.IsSuccessStatusCode)
                {
                    MessageBox.Show($"Error: {response.StatusCode}. Could not retrieve weather data.", "Health Advice Group - Weather Forecast");
                    return;
                }
                response.EnsureSuccessStatusCode();

                string data = response.Content.ReadAsStringAsync().Result;  // Blocking call
                weatherResponse = JsonConvert.DeserializeObject<WeatherResponse>(data);
            }


# API Class

    public class Weather
    {
        [JsonProperty("id")]
        public int Id { get; set; }

        [JsonProperty("main")]
        public string Main { get; set; }

        [JsonProperty("description")]
        public string Description { get; set; }

        [JsonProperty("icon")]
        public string Icon { get; set; }
    }
