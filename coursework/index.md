/* ---------- Coursework: 2-column category grid ---------- */
.course-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  align-items: start;
  margin-top: 16px;
}
.course-col {
  display: flex;
  flex-direction: column;
  gap: 20px;
  min-width: 0; /* prevents grid children from overflowing their track */
}
.course-cat {
  border: 1px solid var(--accent);
  border-radius: 2px;
  padding: 14px 16px;
  background: rgba(206, 170, 250, 0.05);
  overflow-wrap: break-word;
  word-break: break-word;
}
.course-cat h2 {
  margin-top: 0;
  margin-bottom: 10px;
  font-size: 16px;
  border-bottom: 1px dashed var(--accent);
  padding-bottom: 6px;
}
.course-cat p {
  margin: 0 0 10px;
}
.course-cat p:last-child {
  margin-bottom: 0;
}
@media (max-width: 700px) {
  .course-grid {
    grid-template-columns: 1fr;
  }
}
