# Julicord

## Bot Sample

```julia
include("Client.jl")
import .Client

function ready()
    println("good morning")
end

function guildCreate(guild)
    println(guild["id"])
end

Client.on("READY", ready)
Client.on("GUILD_CREATE", guildCreate)

# Obviously you can also do
# Client.on("READY", () -> println("Im ready mommy."))


Client.init("token")
```
