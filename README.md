# Usage
Place glu32.dll in the same folder as the game.
***For Debugging Purposes Only!***  

# Example
```C
#include "glu32.h"

void DoSomething() {
    MessageBox(0, L"Hello from glu32.dll!", L"Emulator glu32.dll", MB_OK);
}

BOOL APIENTRY DllMain( HMODULE hModule,
                       DWORD  ul_reason_for_call,
                       LPVOID lpReserved
                     )
{
    switch (ul_reason_for_call)
    {
    case DLL_PROCESS_ATTACH:
        DoSomething();
    case DLL_THREAD_ATTACH:
    case DLL_THREAD_DETACH:
    case DLL_PROCESS_DETACH:
        break;
    }
    return TRUE;
}


```

