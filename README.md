# Interactive Mixed-Reality Environment Featuring the Chess Player and AI Agent of Engineer and Inventor Leonardo Torres Quevedo

## Information

A script named `torresQuevedoLLMScript.sh` is provided, which allows you to install, update, and delete the model with a custom context.

> [!NOTE]
> By default, the model context is named `leonardo_torres_quevedo_system_context.mf`. This file specifies how the model should behave, which parameters it uses, and which model it is based on.

If no arguments are specified, the script simply checks whether the model exists. To view the list of available arguments, run: 

```shell
./torresQuevedoLLMScript.sh --help
```

## Model Installation

To install the Leonardo Torres Quevedo LLM model, run:

```shell
./torresQuevedoLLMScript.sh --install leonardo_torres_quevedo_system_context.mf
```

For a clean installation (which removes all other models created during installation except `torresQuevedoLLM`), run:

```shell
./torresQuevedoLLMScript.sh --clean --install leonardo_torres_quevedo_system_context.mf
```

## Update Model

To update the model context, run:

```shell
./torresQuevedoLLMScript.sh --update leonardo_torres_quevedo_system_context.mf
```

## Test Connection to the Model

To verify that the model is correctly installed and ready to respond, use the `testModel.sh` script.

> [!NOTE]
> By default, the endpoint `http://localhost:11434/api/chat` and the model name `torresQuevedoLLM` are used.

## Assign IP Address and Port

To run the model on an IP address and port other than `localhost:11434` (the default configuration), you can use the `--ip [IP:PORT]` parameter, as shown below:

```shell
./testModel.sh '--ip 192.168.1.1:11434'
```


### Sending a Prompt to the Model

To send a prompt to the model using the script, run:

```shell
./testModel.sh 'mensaje a enviar entre comillas simples'
```

### Starting a Conversation with the Model

To start a chat with the model in the terminal, run:

```shell
./testModel.sh --chat
```

There are other parameters for configuring the model name or the request endpoint. To view the available options, run:

```shell
./testModel.sh --help
```

## Agent Testing

Some tests have been conducted to verify how the model responds to the provided context:

### Hello, who are you?

I am Leonardo Torres Quevedo, a Spanish engineer and pioneer in automation. Dear visitor, welcome to my laboratory, where I have developed this mechanical marvel known as “El Ajedrecista.”

### Tell me how your invention, “El Ajedrecista,” works.

Sir, my Chess Player is a machine designed to play chess in a specific endgame with its white King and Rook against my black King. It uses relays and electromagnets to make decisions based on the position on the board, always guaranteeing checkmate in fewer than fifty moves. I invite you to experience it for yourself right here.

###  How does the invention work?

Distinguished guest, my Chess Player operates using a system of electronic sensors and actuators. When you place your black king on the board, the electrical contacts beneath the squares detect your opponent’s position, allowing the machine to make logical decisions about how to move my white rook to ensure checkmate in fewer than fifty moves.
