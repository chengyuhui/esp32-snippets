if(CONFIG_NKOLBAN)
    set(COMPONENT_ADD_INCLUDEDIRS cpp_utils)

    list(APPEND COMPONENT_SRCS
        cpp_utils/Task.cpp
        cpp_utils/FreeRTOS.cpp
        cpp_utils/GeneralUtils.cpp
    )

    if(CONFIG_NKOLBAN_BLE)
        list(APPEND COMPONENT_SRCS
            cpp_utils/BLEAddress.cpp
            cpp_utils/BLEAdvertisedDevice.cpp
            cpp_utils/BLEAdvertising.cpp
            cpp_utils/BLECharacteristic.cpp
            cpp_utils/BLECharacteristicMap.cpp
            cpp_utils/BLEClient.cpp
            cpp_utils/BLEDescriptor.cpp
            cpp_utils/BLEDescriptorMap.cpp
            cpp_utils/BLEDevice.cpp
            cpp_utils/BLERemoteCharacteristic.cpp
            cpp_utils/BLERemoteDescriptor.cpp
            cpp_utils/BLERemoteService.cpp
            cpp_utils/BLEScan.cpp
            cpp_utils/BLEServer.cpp
            cpp_utils/BLEService.cpp
            cpp_utils/BLEServiceMap.cpp
            cpp_utils/BLEUUID.cpp
            cpp_utils/BLEUtils.cpp
            cpp_utils/BLEValue.cpp
        )
    endif()

    if(CONFIG_NKOLBAN_BLE2902)
        list(APPEND COMPONENT_SRCS cpp_utils/BLE2902.cpp)
    endif()
endif()

set(COMPONENT_REQUIRES
    "bt"
    "nvs_flash"
)

register_component()