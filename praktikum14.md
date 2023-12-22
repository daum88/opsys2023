Seekord lõin Azure keskkonnas uue virtuaalmasina, kus tegin erinevaid ülesaneid. Oli esmakordne kogemus ja sain üsna okeilt hakkama.

14.1 <img width="842" alt="14 1" src="https://github.com/daum88/opsys2023/assets/68275432/6111eb2e-81f0-4b36-b466-c7796dacbbc3">
14.2 <img width="809" alt="14 2" src="https://github.com/daum88/opsys2023/assets/68275432/0212392f-b5b0-463b-bb5c-fdbf240bf406">
14.3 <img width="866" alt="14 3" src="https://github.com/daum88/opsys2023/assets/68275432/29f8f757-d2e7-4280-b901-3bdaae4d3d6d">
14.4 <img width="849" alt="14 4" src="https://github.com/daum88/opsys2023/assets/68275432/5637ce04-75b6-4912-ae14-e29fbba28bfa">
14.6
#!/bin/bash
git clone https://github.com/AndresNamm/accident
for file in accident/*; do
  grep -q "password" $file
  if [ $? -eq 0 ]; then
    echo "File found: $file"
    cat $file | grep "password"
  fi
done
