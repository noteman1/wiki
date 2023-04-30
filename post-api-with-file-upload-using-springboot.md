```java
@PostMapping("/upload")
public ResponseEntity<String> uploadFile(@RequestParam("file") MultipartFile file) {
    try {
        // Save the uploaded file to disk
        String fileName = file.getOriginalFilename();
        File dest = new File("uploads/" + fileName);
        file.transferTo(dest);
        
        return ResponseEntity.ok("File uploaded successfully");
    } catch (IOException e) {
        e.printStackTrace();
        return ResponseEntity.status(HttpStatus.INTERNAL_SERVER_ERROR).body("Failed to upload file");
    }
}
```