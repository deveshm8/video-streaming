High Level Design:


  User Authentication and Management:
    JWT will be used for user authentication and authorization
  
  Converting uploaded videos into multiple bitrates:
    FFmpeg will be used for adaptive streaming

  Encryption of video:
    Symmetric encryption will be used to encrypt the video

  Network Protocol:
    HLS protocol will be used for streaming video  


https://github.com/deveshm8/video-streaming/assets/60978696/46134591-80cc-47b5-a6e5-b048d1dd1ea1


Low Level Design:


// VideoStorage factory function
const createVideoStorage = (storageBackend) => ({
    storeVideo: (video, transcodedFiles) => {
        // Store video file and metadata
    },
    getVideo: (videoId) => {
        // Retrieve video metadata and file path
        return null;
    }
});

// VideoTranscoding function
const transcodeFunction = (inputFilePath) => {
    // Convert video to multiple bitrate 
};

// EncryptionService factory function
const createEncryption = (encryptionKeyManager) => ({
    encrypt: (inputData) => {
        // Encrypt data using symmetric encryption
    },
    decrypt: (encryptedData) => {
        // Decrypt encrypted data
    }
});

 // Video factory function
const createVideo = (id, title, duration, filePath, transcodedFiles, encrypted) => ({
    id,
    title,
    duration,
    filePath,
    transcodedFiles,
    encrypted
});

// CDN factory function
const createCDN = (cdnService) => ({
    uploadToCDN: (data, url) => {
        // Upload data to CDN and get CDN URL
    }
});

// User create function
const createUser = (id, username, roles) => ({
    id,
    username,
    roles
});

// Authentication function (using jwt)
const AuthenticationService = (authBackend) => ({
    authenticateUser: (credentials) => {
        // Authenticate user and return authentication token
        return jwt token;
    }
});

