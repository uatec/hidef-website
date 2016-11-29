title: RapidRest

---
## Build RESTful services really fast and get on with building your application.

## The Problem

new projects
microservices
dont' want to fanny about with creating an HTTP CRUD API.
Wiring up a data store, often piggy back on another data store
If you do, people don't  

## The Solution

RapidRest
dot net core - cross platform
aspnet middleware
supports HTTP GET, DELETE, PUT, POST and simple queries
Anything more than simple querying and you probably have some other requirement
HAL makes it discoverable
autodiscovery makes configuration trivial
Performance benchmark? 
Competitors?

Event emitter?
## Caveats

not asynchronous

## What you get free 

dev standard in memory storage
mongo db data store

## Getting Started

nuget package
add dotnet core
aspnet

    public class Startup
    {
        // This method gets called by the runtime. Use this method to add services to the container.
        public void ConfigureServices(IServiceCollection services)
        {
            services.AddRapidRest(Assembly.GetEntryAssembly());
        }
        
        public void Configure(IApplicationBuilder app, IHostingEnvironment env)
        {
            app.UseRapidRest();
        }
    }