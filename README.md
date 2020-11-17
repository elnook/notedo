# Notedo

## Usage
Contextual help is available by running `notedo help`

To use the defaults and launch the GUI run:  

```
notedo server --gui
```

To launch with a different host and port

```
notedo server --host 0.0.0.0 -p 8080
```

## Config
Settings can be overridden by CLI flags, environment variables, and the config file (in that order of precedence)

The flag names resemble the equivalent environment variable and config file settings

For example, 
```
$ notedo help
...
Flags:
  -d, --datadir string     Data storage path ...
...
```
To override dataDir you can set the environment variable `NOTEDO_DATADIR=<something>` or in the `notedo.yaml`:
```yaml
datadir: <something>
```
See the contextual help for additional instructions on modifying settings

## Tips
- `Ctrl+P` (`Command+P`) to focus search field
- `Ctrl+Shift+L` (`Command+Shift+L`) to focus search field in `link` mode
- Search supports `slash commands`, start search with `/`
- Search queries use Bleve's [Query String Syntax](http://blevesearch.com/docs/Query-String-Query/), few examples:
  - `note` will find instances of `note`, `Note`, `notes`, `Notes`, etc.
  - `note*` will find the same but also non-stemmed words, such as `Notedo`
- Notedo is a Progress Web App (PWA)!