# simple-sounds

Simple repo for hosting simple sounds.

Inspired by https://github.com/jesserockz/esphome-components

```yaml
speaker:
  - platform: ...
    id: my_speaker
    ...

file:
  - id: my_file
    file: my_file.wav
  - id: my_remote_wav
    file: https://example.com/my_file.wav

button:
  - platform: template
    name: Play my file
    on_press:
      - lambda: id(my_speaker).play(id(my_file), sizeof(id(my_file)));
```
