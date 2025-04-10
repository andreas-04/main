# Use the Dockerfile to build your Next.js app
docker_build('folio-client', '.', dockerfile='Dockerfile')

# Define the resource for the app
k8s_resource('folio-client', port_forwards=3000)
