# Autotyper
function autotypeInDiscord(message) {
    /**
     * This function simulates typing a message in Discord.
     * 
     * Parameters:
     * message (string): The message to be typed in Discord.
     * 
     * Returns:
     * string: The simulated typing message in Discord.
     */
    
    try {
        // Check if the message is a string
        if (typeof message !== 'string') {
            throw new TypeError("Message must be a string");
        }
        
        // Simulate typing
        let typingMessage = "";
        for (let i = 0; i < message.length; i++) {
            typingMessage += message[i];
            // Delay between each character
            await new Promise(resolve => setTimeout(resolve, 1000));
        }
        
        return typingMessage;
    } catch (error) {
        // Log the error
        console.error("Error:", error);
        return "";
    }
}
