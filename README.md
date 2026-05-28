import React, { useRef } from 'react';
import { Canvas, useFrame } from '@react-three/fiber';
import { Environment, Float, Center } from '@react-three/drei';

// Individual Interactive 3D Card / Shape Component
function ChromeWidget({ geometryType = 'roundedBox' }) {
  const meshRef = useRef();

  // Subtle rotation animation loop that runs every single frame
  useFrame((state) => {
    const time = state.clock.getElapsedTime();
    if (meshRef.current) {
      meshRef.current.rotation.x = Math.sin(time / 3) * 0.2;
      meshRef.current.rotation.y = time * 0.15;
    }
  });

  return (
    // Float handles smooth, organic hovering physics up and down
    <Float speed={3} rotationIntensity={0.5} floatIntensity={0.8}>
      <mesh ref={meshRef} castShadow receiveShadow>
        
        {/* Dynamic Geometry Selector */}
        {geometryType === 'torus' ? (
          <torusKnotGeometry args={[0.8, 0.25, 160, 16]} />
        ) : geometryType === 'sphere' ? (
          <sphereGeometry args={[1, 64, 64]} />
        ) : (
          // Default sleek rounded display panel card
          <boxGeometry args={[2.2, 1.4, 0.2]} />
        )}

        {/* --- PREMIUM METALLIC CHROMATIC MATERIAL --- */}
        <meshPhysicalMaterial
          color="#f4f7fc"               // Clear mirror titanium base tint
          roughness={0.01}              // Ultra-glossy, flawless reflective surface
          metalness={1.0}              // 100% metallic properties
          clearcoat={1.0}              // Secondary hard outer clear lacquer shell
          clearcoatRoughness={0.0}
          
          // --- OIL-SLICK CHROMATIC GRADIENT ENGINE ---
          iridescence={1.0}            // Activates shifting rainbow refraction
          iridescenceIOR={2.1}         // High Index of Refraction for deep gradient bands
          iridescenceThicknessRange={[100, 600]} // Blends the magenta-to-cyan color transitions
          
          // --- HIGHLIGHT INTENSITY ---
          envMapIntensity={3.5}        // Drastically brightens the gradient reflections
        />
      </mesh>
    </Float>
  );
}

// Main Canvas Layout Configuration
export default function App() {
  return (
    <div style={{ width: '100vw', height: '100vh', background: '#050507', overflow: 'hidden' }}>
      <Canvas camera={{ position: [0, 0, 4.5], fov: 45 }}>
        
        {/* Deep background ambient space so reflections stand out */}
        <ambientLight intensity={0.1} />
        
        {/* --- THE CHROMATIC STUDIO LIGHT CAGE --- */}
        {/* Front-Left Accent: High-energy Neon Cyan Light */}
        <directionalLight position={[-8, 6, 4]} intensity={3.0} color="#00ffff" />
        
        {/* Front-Right Accent: High-contrast Hot Magenta Light */}
        <directionalLight position={[8, -6, 3]} intensity={3.5} color="#ff00ff" />
        
        {/* Top/Back Rim Accent: Royal Electric Purple for edge popping */}
        <directionalLight position={[0, 8, -4]} intensity={2.5} color="#7b00ff" />
        
        {/* --- WIDGET DISPLAY LAYOUT --- */}
        <Center>
          {/* You can duplicate this or map over your divisions (Youssef, Samah, Akiro) */}
          <group position={[0, 0, 0]}>
            <ChromeWidget geometryType="torus" />
          </group>
        </Center>

        {/* Real studio reflection environment profiles */}
        <Environment preset="studio" />
        
      </Canvas>
    </div>
  );
}
