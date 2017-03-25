# Blitzy

## Description
A load tester that distributes processing across nodes. Based on example in The Little Elixir and OTP Guidebook.

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `blitzy` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [{:blitzy, "~> 0.1.0"}]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/blitzy](https://hexdocs.pm/blitzy).

## Setup

To build the application you need to run 
`mix escript.build`
To generate an executable script.

## Run

Spawn three seperate nodes in seperate terminals with the following:
`iex --name b@127.0.0.1 -S mix`
`iex --name c@127.0.0.1 -S mix`
`iex --name d@127.0.0.1 -S mix`

Run the Blitzy like this:
`./blitzy -n N URL`

Where `N` is a positive integer to specify the amount of requests and `URL` is the url to hit.

For example:
`./blitzy -n 10000 http://mysite.com`