# WHV_EMULATOR_STATUS
**Note: A prerelease of this API is available starting in the Windows Insiders Preview Build 17083**

## Syntax

```c
typedef union _WHV_EMULATOR_STATUS
{
    struct
    {
        UINT32 EmulationSuccessful : 1;
        UINT32 InternalEmulationFailure : 1;
        UINT32 IoPortCallbackFailed : 1;
        UINT32 MemoryCallbackFailed : 1;
        UINT32 TranslateGvaPageCallbackFailed : 1;
        UINT32 TranslateGvaPageCallbackGpaPageIsNotAligned : 1;
        UINT32 GetVirtualProcessorRegistersCallbackFailed : 1;
        UINT32 SetVirtualProcessorRegistersCallbackFailed : 1;
        UINT32 InterruptCausedIntercept : 1;
        UINT32 GuestCannotBeFaulted : 1;
        UINT32 Reserved : 21;
    };

    UINT32 AsUINT32;
} WHV_EMULATOR_STATUS;
```
## Remarks
Describes extended return status information from a given emulation call.
