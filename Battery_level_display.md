### 在手机连接蓝牙的时候显示电池电量
* 在所建的蓝牙工程中寻找如下文件：D:\Project\3026sink-amazon-avs\apps\applications\sink\module_configurations\sink_hfp_data_def
* 替换粘贴以下AT指令
```
    <ConfigGroup
        Id="HFP AT Commands Data"
        ShortId="sink_hfp_at_commands"
        Node="Array"
        ConfigGroupPath="./[@ShortId='advanced_settings']/[@ShortId='at_commands_key']/[@ShortId='command_data']">
        <ConfigPatternArray
            Id="AT command raw data"
            ShortId="at_commands"
            Pattern="at_command_data"
            MaxNumPatterns="60" >
 <PatternArrayRow Id="AT Data Row1" ShortId="at_data_row_1" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2b4d" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row2" ShortId="at_data_row_2" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4943" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row3" ShortId="at_data_row_3" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x5445" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row4" ShortId="at_data_row_4" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x5354" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row5" ShortId="at_data_row_5" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x004f" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row6" ShortId="at_data_row_6" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4b0d" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row7" ShortId="at_data_row_7" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x002b" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row8" ShortId="at_data_row_8" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x5841" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row9" ShortId="at_data_row_9" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x504c " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row10" ShortId="at_data_row_10" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x3d69 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row11" ShortId="at_data_row_11" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x5068 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row12" ShortId="at_data_row_12" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x6f6e " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row13" ShortId="at_data_row_13" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x652c " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row14" ShortId="at_data_row_14" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x3700 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row15" ShortId="at_data_row_15" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4f4b " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row16" ShortId="at_data_row_16" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x0d00 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row17" ShortId="at_data_row_17" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4154 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row18" ShortId="at_data_row_18" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2b58 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row19" ShortId="at_data_row_19" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4150 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row20" ShortId="at_data_row_20" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4c3d " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row21" ShortId="at_data_row_21" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x3035 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row22" ShortId="at_data_row_22" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4143 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row23" ShortId="at_data_row_23" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2d31 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row24" ShortId="at_data_row_24" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x3730 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row25" ShortId="at_data_row_25" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x322d " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row26" ShortId="at_data_row_26" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x3031 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row27" ShortId="at_data_row_27" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x3030 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row28" ShortId="at_data_row_28" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2c37 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row29" ShortId="at_data_row_29" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x0d00 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row30" ShortId="at_data_row_30" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4154 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row31" ShortId="at_data_row_31" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2b49 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row32" ShortId="at_data_row_32" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x5048 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row33" ShortId="at_data_row_33" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4f4e " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row34" ShortId="at_data_row_34" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4541 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row35" ShortId="at_data_row_35" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4343 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row36" ShortId="at_data_row_36" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x4556 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row37" ShortId="at_data_row_37" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x3d32 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row38" ShortId="at_data_row_38" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2c31 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row39" ShortId="at_data_row_39" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2c82 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row40" ShortId="at_data_row_40" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2c32 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row41" ShortId="at_data_row_41" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x2c30 " />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row42" ShortId="at_data_row_42" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x0d00" />
 </PatternArrayRow>
 <PatternArrayRow Id="AT Data Row43" ShortId="at_data_row_43" Node="Basic">
 <PatternArrayConfigItem ShortId="data" DefaultValue="0x0000" />
 </PatternArrayRow>
        </ConfigPatternArray>
  
    </ConfigGroup>

    <ConfigGroup
        Id="Event to AT Commands Mapping"
        ShortId="sink_hfp_event_at_command_table"
        Node="Array"
        ConfigGroupPath="./[@ShortId='advanced_settings']/[@ShortId='at_commands_key']/[@ShortId='event_to_at_command_mapping']" >
        <ConfigPatternArray
            Id="Event to AT Command Mapping Definition"
            ShortId="event_at_commands"
            Pattern="at_commands_events"
            MaxNumPatterns="10"  >
          <PatternArrayRow Id="AT Event Row1" ShortId="at_event_row_1" Node="Basic">
          <PatternArrayConfigItem ShortId="event" DefaultValue="SLC Connected" />
          <PatternArrayConfigItem ShortId="at_cmd" DefaultValue="0x0004" />
          </PatternArrayRow>
          <PatternArrayRow Id="AT Event Row2" ShortId="at_event_row_2" Node="Basic">
          <PatternArrayConfigItem ShortId="event" DefaultValue="SLC Connected" />
         <PatternArrayConfigItem ShortId="at_cmd" DefaultValue="0x0005" />
         </PatternArrayRow>
         <PatternArrayRow Id="AT Event Row3" ShortId="at_event_row_3" Node="Basic">
         <PatternArrayConfigItem ShortId="event" DefaultValue="Gas Gauge 0" />
         <PatternArrayConfigItem ShortId="at_cmd" DefaultValue="0x0005" />
         </PatternArrayRow>
         <PatternArrayRow Id="AT Event Row4" ShortId="at_event_row_4" Node="Basic">
         <PatternArrayConfigItem ShortId="event" DefaultValue="Gas Gauge 1" />
         <PatternArrayConfigItem ShortId="at_cmd" DefaultValue="0x0005" />
         </PatternArrayRow>
         <PatternArrayRow Id="AT Event Row5" ShortId="at_event_row_5" Node="Basic">
         <PatternArrayConfigItem ShortId="event" DefaultValue="Charger Gas Gauge 0" />
         <PatternArrayConfigItem ShortId="at_cmd" DefaultValue="0x0005" />
         </PatternArrayRow>
         <PatternArrayRow Id="AT Event Row6" ShortId="at_event_row_6" Node="Basic">
         <PatternArrayConfigItem ShortId="event" DefaultValue="Charger Gas Gauge 3" />
         <PatternArrayConfigItem ShortId="at_cmd" DefaultValue="0x0005" />
         </PatternArrayRow>
         </ConfigPatternArray>    
</ConfigGroup>
```
* clean all后重新Build all