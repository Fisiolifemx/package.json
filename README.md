'use client'
import { motion } from "framer-motion";

export default function Page() {

  const whatsapp = "https://wa.me/525582606593?text=Gracias%20por%20comunicarse%20con%20FISIOLIFE%20MX.%20%C2%BFEn%20qu%C3%A9%20podemos%20ayudarle%3F";
  const maps = "https://www.google.com/maps/search/?api=1&query=Villa+del+Real+Tecamac";

  return (
    <div style={{fontFamily:'Segoe UI, sans-serif', margin:0, background:'#f1f5f9', color:'#0f172a'}}>

      {/* BOTÓN WHATSAPP */}
      <a href={whatsapp} target="_blank" style={{
        position:'fixed', bottom:25, right:25,
        background:'#16a34a', color:'white',
        padding:18, borderRadius:'50%',
        fontSize:22, boxShadow:'0 6px 20px rgba(0,0,0,0.3)'
      }}>💬</a>

      {/* HERO */}
      <section style={{
        background:'linear-gradient(120deg,#020617,#1e3a8a)',
        color:'white', textAlign:'center',
        padding:'130px 20px'
      }}>
        <motion.h1 initial={{opacity:0,y:-30}} animate={{opacity:1,y:0}} style={{fontSize:38}}>
          Recupere su movilidad con fisioterapia profesional en Tecámac
        </motion.h1>

        <p style={{fontSize:18, opacity:0.9}}>
          Atención especializada, tratamientos personalizados y resultados reales
        </p>

        <div style={{marginTop:30}}>
          <a href={whatsapp} target="_blank" style={{
            background:'#22c55e', padding:'14px 22px',
            color:'white', borderRadius:12, marginRight:10,
            fontWeight:'bold'
          }}>
            Agende su cita por WhatsApp
          </a>

          <a href={maps} target="_blank" style={{
            background:'white', padding:'14px 22px',
            color:'#020617', borderRadius:12
          }}>
            Cómo llegar
          </a>
        </div>

        <p style={{marginTop:15, fontSize:14}}>
          Atención con previa cita | Cupo limitado
        </p>
      </section>

      {/* GALERÍA PREMIUM */}
      <section style={{padding:60}}>
        <h2 style={{textAlign:'center'}}>Instalaciones</h2>

        <div style={{
          display:'grid',
          gridTemplateColumns:'repeat(auto-fit,minmax(250px,1fr))',
          gap:20
        }}>
          {["img1.jpg","img2.jpg","img3.jpg","img4.jpg","img5.jpg"].map((img,i)=>(
            <motion.img
              key={i}
              src={"/"+img}
              initial={{opacity:0,scale:0.95}}
              whileInView={{opacity:1,scale:1}}
              style={{width:'100%', borderRadius:15, boxShadow:'0 8px 20px rgba(0,0,0,0.15)'}}
            />
          ))}
        </div>
      </section>

      {/* DIFERENCIADOR */}
      <section style={{padding:60, background:'#e2e8f0'}}>
        <h2>No solo tratamos el dolor</h2>
        <p>
          Nuestro enfoque está en identificar la causa del problema para lograr una recuperación completa y duradera.
        </p>
      </section>

      {/* MISIÓN */}
      <section style={{padding:60}}>
        <h2>Misión</h2>
        <p>
          Brindar un servicio de fisioterapia integral, enfocado en escuchar, entender y acompañar a cada paciente en su proceso de recuperación. 
          Nuestra misión es aliviar el dolor, restaurar el movimiento y mejorar la calidad de vida, a través de tratamientos personalizados, 
          basados en la empatía, la ciencia y el compromiso con el bienestar físico y emocional de cada persona.
        </p>
      </section>

      {/* VISIÓN */}
      <section style={{padding:60, background:'#e2e8f0'}}>
        <h2>Visión</h2>
        <p>
          Convertirnos en una clínica líder en rehabilitación física y bienestar integral, reconocida por la excelencia en nuestros tratamientos, 
          la innovación en nuestras técnicas terapéuticas y el compromiso humano con cada paciente, promoviendo una cultura de salud, movimiento 
          y calidad de vida.
        </p>
      </section>

      {/* VALORES */}
      <section style={{padding:60}}>
        <h2>Valores</h2>
        <ul style={{lineHeight:2}}>
          <li><b>Empatía:</b> Escuchamos y comprendemos las necesidades de cada paciente.</li>
          <li><b>Compromiso:</b> Damos nuestro máximo esfuerzo en cada sesión.</li>
          <li><b>Profesionalismo:</b> Atención ética y basada en evidencia.</li>
          <li><b>Vocación de servicio:</b> Trabajamos con pasión por su bienestar.</li>
          <li><b>Trabajo en equipo:</b> Colaboración para mejores resultados.</li>
          <li><b>Innovación:</b> Técnicas modernas y actualizadas.</li>
          <li><b>Confianza:</b> Ambiente seguro y motivador.</li>
        </ul>
      </section>

      {/* SERVICIOS */}
      <section style={{padding:60, background:'#e2e8f0'}}>
        <h2>Servicios especializados</h2>
        <ul>
          <li>Rehabilitación deportiva</li>
          <li>Ortopédica y traumatológica</li>
          <li>Pediatría</li>
          <li>Medicina del dolor</li>
        </ul>

        <a href={whatsapp} target="_blank" style={{
          background:'#16a34a',
          color:'white',
          padding:12,
          borderRadius:10
        }}>
          Solicitar información
        </a>
      </section>

      {/* TESTIMONIOS */}
      <section style={{padding:60}}>
        <h2>Opiniones de pacientes</h2>
        <p>"Recibí una atención excelente y mejoré notablemente" ⭐⭐⭐⭐⭐</p>
        <p>"Profesionalismo y trato humano en todo momento" ⭐⭐⭐⭐⭐</p>
      </section>

      {/* UBICACIÓN */}
      <section style={{padding:60, background:'#e2e8f0'}}>
        <h2>Ubicación</h2>
        <p>Villa del Real, Tecámac — fácil acceso y atención cercana</p>

        <iframe
          src="https://www.google.com/maps?q=Villa+del+Real+Tecamac&output=embed"
          style={{width:'100%', height:300, borderRadius:15}}
        />
      </section>

      <footer style={{textAlign:'center', padding:25}}>
        FisioLife MX © 2026 | Clínica de fisioterapia en Tecámac
      </footer>

    </div>
  )
}