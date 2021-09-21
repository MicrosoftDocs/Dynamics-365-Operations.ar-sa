---
title: لا يكتمل سير عمل دفتر يومية المخزون أبدًا ولا يمكن معالجة دفتر اليومية
description: بعد إرسال سير عمل اعتماد دفتر اليومية، تتوقف معالجه سير العمل عن الاستجابة، ولا يمكنك تحرير دفاتر اليومية أو معالجتها.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475434"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>لا يكتمل سير عمل دفتر يومية المخزون أبدًا ولا يمكن معالجة دفتر اليومية

## <a name="symptoms"></a>العلامات

بعد إرسال سير عمل اعتماد دفتر اليومية، تتوقف معالجه سير العمل عن الاستجابة، ولا يمكنك تحرير دفاتر اليومية أو معالجتها.

## <a name="resolution"></a>الحل

هناك العديد من الأسباب التي قد لا يتم إكمال معالجه سير العمل فيها. التحقق من المشكلات التالية:

- انتقل إلى **أداره المخزون &gt; اعداد &gt; عمليات سير عمل الاداره**، وقم بمراجعه تكوين سير العمل المتاثر. لمزيد من المعلومات ، راجع [عمليات سير عمل اعتماد دفتر يوميه المخزون](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md).
- قد يواجه سير العمل استثناءا أو خطا. قم بمراجعه سجل عنصر العمل الخاص بسير العمل المتاثر لمعرفه ما إذا كان يتضمن خطا في التطبيق الذي ينهي سير العمل.
- يمكن تحديث دفتر يوميه المخزون أو تحريره فقط في حاله اعتماده. وإذا كان الاسترجاع نشطا، فيمكنك محاولة استدعاء دفتر اليومية. قد يتم إيقاف تنفيذ وظيفة مجموعه سير العمل مؤقتا لأسباب متعددة. قد تحدث بعض هذه الأسباب بسبب مشكله اطار عمل سير العمل.
