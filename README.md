<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>โปรเจกต์ 3D แรกของฉัน 🎲</title>
    <style>
        body {
            margin: 0;
            overflow: hidden; /* ซ่อนสกรอลล์บาร์ */
            background-color: #000;
        }
        #info {
            position: absolute;
            top: 20px;
            width: 100%;
            text-align: center;
            color: white;
            font-family: sans-serif;
            font-size: 18px;
            pointer-events: none;
        }
    </style>
    <!-- ดึง Three.js มาใช้งานผ่าน CDN -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
</head>
<body>

    <div id="info">🎲 กล่อง 3D หมุนได้ตัวแรกบนหน้าเว็บ!</div>

    <script>
        // 1. สร้าง ฉาก (Scene), กล้อง (Camera) และ ตัววาดภาพ (Renderer)
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({ antialias: true });

        renderer.setSize(window.innerWidth, window.innerHeight);
        document.body.appendChild(renderer.domElement);

        // 2. สร้างวัตถุ 3D (รูปทรง + พื้นผิว/สี)
        const geometry = new THREE.BoxGeometry(2, 2, 2); // รูปทรงลูกบาศก์ขนาด 2x2x2
        const material = new THREE.MeshStandardMaterial({ color: 0x00ff88, roughness: 0.3 }); // สีเขียวนีออนสะท้อนแสง
        const cube = new THREE.Mesh(geometry, material);
        scene.add(cube);

        // 3. ใส่แสงสว่างลงในฉาก (ถ้าไม่มีแสง วัตถุจะมืดมองไม่เห็น)
        const light = new THREE.DirectionalLight(0xffffff, 1);
        light.position.set(5, 5, 5).normalize();
        scene.add(light);

        const ambientLight = new THREE.AmbientLight(0x404040); // แสงสว่างรอบๆ
        scene.add(ambientLight);

        // วางตำแหน่งกล้องถอยออกมาให้มองเห็นกล่อง
        camera.position.z = 5;

        // 4. แอนิเมชันสั่งให้กล่องหมุนตลอดเวลาแบบเรียลไทม์
        function animate() {
            requestAnimationFrame(animate);

            // ปรับมุมหมุนทีละนิด
            cube.rotation.x += 0.01;
            cube.rotation.y += 0.01;

            renderer.render(scene, camera);
        }

        animate();

        // ปรับขนาดหน้าจออัตโนมัติเมื่อย่อ/ขยายเบราว์เซอร์
        window.addEventListener('resize', () => {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        });
    </script>

</body>
</html>
