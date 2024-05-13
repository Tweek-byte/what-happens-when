Table of Contents

    The "g" key is pressed
        Upon pressing the "g" key, the browser receives the event, triggering auto-complete functions.
        Depending on browser algorithms and browsing mode, various suggestions are presented, sorted based on history, bookmarks, cookies, and internet-wide popular searches.
        As "google.com" is typed, the suggestions refine with each keypress, potentially suggesting the complete URL before it's fully typed.

    The "enter" key bottoms out
        When the "enter" key is pressed, an electrical circuit specific to the key is closed, allowing current flow into the keyboard's logic circuitry.
        The keyboard controller scans the state of each key switch, debounces the noise, and converts it into a keycode integer (e.g., 13 for "enter").
        The keycode is stored and transmitted via USB or Bluetooth to the computer, where it's decoded and passed to the operating system's hardware abstraction layer.

    Interrupt fires (not applicable for USB keyboards)
        The keyboard sends signals on its interrupt request line (IRQ), mapped to an interrupt vector by the interrupt controller.
        The CPU uses the Interrupt Descriptor Table (IDT) to run the appropriate kernel-supplied interrupt handler.

    OS-specific actions
        On Windows, a WM_KEYDOWN message is sent to the application.
        On macOS, a KeyDown NSEvent is sent to the app.
        On GNU/Linux, the Xorg server listens for keycodes and passes them to the window manager, which then sends them to the focused window.

    Parse URL
        The browser parses the URL, extracting the protocol ("http") and resource ("/").

    Check HSTS list
        The browser checks its preloaded HSTS list to determine if the website should be contacted via HTTPS.

    DNS lookup
        The browser checks its DNS cache and performs a DNS lookup if necessary, querying the DNS server configured in the network stack.

    ARP process
        If the DNS server's IP is on a different subnet, the ARP process resolves the MAC address of the default gateway.

    Opening of a socket
        The browser establishes a TCP socket stream to the destination server.

    TLS handshake
        If HTTPS is used, a TLS handshake occurs between the client and server to establish a secure connection.

    HTTP protocol
        The browser sends an HTTP request to the server, requesting the desired resource.

    HTTP Server Request Handle
        The server handles the HTTP request, processing it according to its configuration and returning the appropriate response.

    Page Rendering
        The browser parses HTML, CSS, and JavaScript to construct and render the page.

    GPU Rendering
        Graphics processing units (GPUs) may be used for rendering graphics-intensive content.

    Window Server
        Post-rendering, the browser executes JavaScript and handles user-induced interactions.
