# Deploying-a-Node.js-Application-on-AWS
Deploying a Node.js Application on AWS
# Node.js Application

This is a simple Node.js application deployed on AWS EC2 using Ubuntu.

## Steps to Deploy on AWS

1. **Launch an EC2 Instance:** Start an Ubuntu EC2 instance on AWS.
2. **Connect to the Instance:**
   ```sh
   ssh -i your-key.pem ubuntu@your-ec2-ip
   ```
3. **Update and Install Dependencies:**
   ```sh
   sudo apt update && sudo apt upgrade -y
   sudo apt install -y nodejs npm git
   ```
4. **Clone the Repository:**
   ```sh
   git clone <repository-url>
   cd <project-directory>
   ```
5. **Install Project Dependencies:**
   ```sh
   npm install
   ```
6. **Create and Configure Environment Variables:**
   ```sh
   touch .env
   nano .env
   ```
   Add required variables:
   ```
   PORT=3000
   DB_URI=<your-database-uri>
   ```
7. **Start the Server:**
   ```sh
   npm start
   ```
8. **Update Security Group:** Ensure inbound rules allow traffic on your application port (e.g., 3000).

## License

This project is licensed under the MIT License.
