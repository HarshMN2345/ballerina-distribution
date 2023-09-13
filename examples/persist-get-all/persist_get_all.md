# Persist read - Get all records

The bal persist feature provides support to manage data persistence in a Ballerina package. It starts with defining the application's data model. Once the model is defined, the client API is generated with resources based on the model. The generated API can be used to query and manipulate the persistent data in the application.

The generated client API provides a `get` resource method to retrieve all records from the data store.

> **Note:** This example uses Ballerina tables as the data store. You can use MySQL and Google Sheets as the data store as well. For more information, see [Supported Data Stores](/learn/supported-data-stores/).

#### Initialize the project
Execute the command below to initialize `bal persist` in the project.

::: out persist_init.out :::

#### Model the data

Add `Employee` entity with the following fields in the `model.bal` file inside the `persist` directory.

::: code persist_model.bal :::

#### Generate client APIs
Execute the command below to generate the Ballerina client API.

::: out persist_generate.out :::

#### Use the generated client API

Using the generated client API, we can retrieve all records from the data store. The `get` resource method returns a stream of records. We can iterate through the stream and print the records.

::: code persist_get_all.bal :::

#### Run the program

Execute the command below to run the program.

::: out persist_get_all.out :::
