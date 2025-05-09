podman build -t terraform-image .

podman run -it \
  -e AWS_ACCESS_KEY_ID=your_access_key \
  -e AWS_SECRET_ACCESS_KEY=your_secret_key \
  -e AWS_SESSION_TOKEN=your_session_token \  # Only if you're using temporary credentials
  -e AWS_DEFAULT_REGION=your_region \        # e.g., us-east-1
  your-image-name