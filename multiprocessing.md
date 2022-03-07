thread = threading.Thread(...)
args : target, args
thread.start()
thread.join() -> ce qui suit n'est pas exécuté avant la fin des threads
lock.acquire(), lock.release() où lock = threading.Lock()
import multiprocessing -> can be terminated (terminate or kill), puis close
** if __name__ == "__main__":  # Très important pour des raisons techniques
multiprocessing.Lock()
multiprocessing offre Pool : même tâche sur plusieurs processus
distribuer le travail : map, starmap, apply (versions synchrone ou asynchrone)
with multiprocessing.Pool(nbProcesses) as pool: ...
instances de classe (héritage) -> attributs et méthodes selon nos besoins
ne pas oublier dans class __init__: super(myThread, self).__init__()
si attribut stop par exemple, ne pas join car sinon process ne se rendra jamais au stop
multiprocessing et multithreading avec CPUs vs GPU pour matrices surtout et opérations similaires (GPU pas pour boucles d'opérations)
