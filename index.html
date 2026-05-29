<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CHROMA STUDIO</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            background-color: #050507;
            overflow: hidden;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #ffffff;
            width: 100vw;
            height: 100vh;
        }
        /* Absolute UI Overlay */
        .header {
            position: absolute;
            top: 5%;
            width: 100%;
            text-align: center;
            z-index: 10;
            pointer-events: none;
        }
        .header h1 {
            font-size: 2.8rem;
            letter-spacing: 8px;
            margin-bottom: 5px;
            font-weight: 800;
            text-shadow: 0 0 20px rgba(0, 255, 255, 0.2);
        }
        .header p {
            opacity: 0.5;
            font-size: 0.9rem;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        #canvas-container {
            width: 100%;
            height: 100%;
        }
    </style>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
</head>
<body>

    <div class="header">
        <h1>⚡ CHROMA ⚡</h1>
        <p>Creative Collective Studio Portfolio</p>
    </div>

    <div id="canvas-container"></div>

    <script>
        // --- 1. SETUP SCENE, CAMERA & RENDERER ---
        const container = document.getElementById('canvas-container');
        const scene = new THREE.Scene();
        scene.background = new THREE.Color('#050507');

        const camera = new THREE.PerspectiveCamera(50, window.innerWidth / window.innerHeight, 0.1, 1000);
        camera.position.z = 6;

        const renderer = new THREE.WebGLRenderer({ antialias: true });
        renderer.setSize(window.innerWidth, window.innerHeight);
        renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
        renderer.toneMapping = THREE.ACESFilmicToneMapping;
        renderer.toneMappingExposure = 1.2;
        container.appendChild(renderer.domElement);

        // --- 2. CHROMATIC NEON GRADIENT LIGHT CAGE ---
        const ambientLight = new THREE.AmbientLight('#111116', 0.5);
        scene.add(ambientLight);

        // Front-Left: Intense Cyan
        const cyanLight = new THREE.DirectionalLight('#00ffff', 3.5);
        cyanLight.position.set(-8, 5, 4);
        scene.add(cyanLight);

        // Front-Right: Hot Magenta
        const magentaLight = new THREE.DirectionalLight('#ff00ff', 4.0);
        magentaLight.position.set(8, -5, 3);
        scene.add(magentaLight);

        // Top-Back Rim: Electric Royal Purple
        const purpleLight = new THREE.DirectionalLight('#7b00ff', 3.0);
        purpleLight.position.set(0, 6, -4);
        scene.add(purpleLight);

        // --- 3. THE LIQUID CHROME MATERIAL ENGINE ---
        // Generates a mirror-finish titanium layer with iridescent properties
        const chromeMaterial = new THREE.MeshPhysicalMaterial({
            color: new THREE.Color('#f4f7fc'),
            roughness: 0.02,
            metalness: 1.0,
            clearcoat: 1.0,
            clearcoatRoughness: 0.0,
            reflectivity: 1.0
        });

        // --- 4. GEOMETRIES FOR THE 3 DIVISIONS ---
        const widgets = [];

        // Youssef (GFX) - Card Panel
        const gfxGeo = new THREE.BoxGeometry(1.8, 1.2, 0.2);
        const gfxMesh = new THREE.Mesh(gfxGeo, chromeMaterial);
        gfxMesh.position.x = -2.6;
        scene.add(gfxMesh);
        widgets.push({ mesh: gfxMesh, speedX: 0.4, speedY: 0.3, offset: 0 });

        // Samah (ART) - Perfect Sphere
        const artGeo = new THREE.SphereGeometry(0.8, 64, 64);
        const artMesh = new THREE.Mesh(artGeo, chromeMaterial);
        artMesh.position.x = 0;
        scene.add(artMesh);
        widgets.push({ mesh: artMesh, speedX: 0.2, speedY: 0.5, offset: Math.PI / 2 });

        // Akiro (VFX) - Complex Torus Knot
        const vfxGeo = new THREE.TorusKnotGeometry(0.55, 0.18, 150, 16);
        const vfxMesh = new THREE.Mesh(vfxGeo, chromeMaterial);
        vfxMesh.position.x = 2.6;
        scene.add(vfxMesh);
        widgets.push({ mesh: vfxMesh, speedX: 0.5, speedY: 0.2, offset: Math.PI });

        // --- 5. ANIMATION ENGINE (FLUID ROTATION & HOVER LOOP) ---
        const clock = new THREE.Clock();

        function animate() {
            requestAnimationFrame(animate);
            const time = clock.getElapsedTime();

            widgets.forEach((widget) => {
                // Organic floating hover up & down
                widget.mesh.position.y = Math.sin(time * 1.5 + widget.offset) * 0.15;
                
                // Continuous liquid chrome reflection slide loop
                widget.mesh.rotation.x = Math.sin(time * widget.speedX) * 0.2;
                widget.mesh.rotation.y = time * widget.speedY;
            });

            renderer.render(scene, camera);
        }
        animate();

        // --- 6. WINDOW RESIZE HANDLING ---
        window.addEventListener('resize', () => {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        });
    </script>
</body>
</html>
