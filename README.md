<!--
  If you have any question about this then raise an issue at https://github.com/mbed-ce-libraries-examples/LibraryTemplate/issues
  
  Under this block replace the text with a name of new library and some short description.
-->
# Custom_target_example
This example demonstrate how to run custom targets under MbedCE as an example we show Bluepill
![stm32f103c8t6_pinout_voltage01](https://github.com/user-attachments/assets/d2a98f4a-a873-4296-9622-f715067ff497)

<!--
  Under this block edit How to start with the library under MbedCE
-->
## How to start
This guide assumes you are familiar with the MbedCE build system, if not, please visit https://github.com/mbed-ce/mbed-os/wiki
1. Open OS Command line and navigate to your workspace, for exampe `C:\MbedCE_projects\`
2. Into Command line type
  - `git clone --no-recurse-submodules https://github.com/mbed-ce-libraries-examples/Custom_target_example.git HerePlaceMyProjectName`
  - `cd HerePlaceMyProjectName && git submodule update --init -- mbed-os custom_targets`
  - if you want to move MbedOS to the latest tracked commit without fetching nested submodules inside `mbed-os`, use `git submodule update --remote -- mbed-os`
  - nested submodules inside `mbed-os` are intentionally not downloaded here because the build system handles them automatically
3. On the last line of *cmake-variants.yaml* file set your [upload method](https://github.com/mbed-ce/mbed-os/wiki/Upload-Methods). Default is NONE = it generates just .bin file. Optimal for external loaders like DFU method and so on (I personaly prefer [STM32CUBE](https://github.com/mbed-ce/mbed-os/wiki/Upload-Methods#stm32cube)). 
4. Build the project
