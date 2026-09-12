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
  min-width: 0;
}
.course-cat {
  border: 1px solid var(--accent);
  border-radius: 2px;
  padding: 14px 16px;
  background: rgba(206, 170, 250, 0.05);
  overflow-wrap: break-word;
  word-break: break-word;
  font-size: 13px;
}
.course-cat h2 {
  margin-top: 0;
  margin-bottom: 8px;
  font-size: 15px;
  border-bottom: 1px dashed var(--accent);
  padding-bottom: 6px;
}
.course-cat ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
.course-cat li {
  padding: 3px 0;
  line-height: 1.3;
}
.course-cat li + li {
  border-top: 1px dotted rgba(206, 170, 250, 0.25);
}
@media (max-width: 700px) {
  .course-grid {
    grid-template-columns: 1fr;
  }
}
