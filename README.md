# Sidekiq

## What is it?
Framework that handles background jobs

## How is it included?

Include it in your gem file:

```
gem 'sidekiq'
```

## Getting Started

### Configure ActiveJobs to use sidekiq
```
class Application < Rails::Application
  # ...
  config.active_job.queue_adapter = :sidekiq
end
```

### Generate new job
```
rails generate job Example
```

### Tell generated job to do something
```
class ExampleJob < ActiveJob::Base
  # Set the Queue as Default
  queue_as :default

  def perform(*args)
    Perform Job
  end
end
```

## Key Features

### + Create jobs anywhere

### + Store jobs data with Redis

### + Pulls automatically from job queue on Redis server

## Example
autogenics-client-project
